
HumanDied = false
local reanim
function noplsmesh(hat)
_G.OldCF=workspace.Camera.CFrame
oldchar=game.Players.LocalPlayer.Character
game.Players.LocalPlayer.Character=workspace[game.Players.LocalPlayer.Name]
for i,v in next, workspace[game.Players.LocalPlayer.Name][hat]:GetDescendants() do
if v:IsA('Mesh') or v:IsA('SpecialMesh') then
v:Remove()
end
end
game.Players.LocalPlayer.Character=oldchar
wait()
workspace.Camera.CFrame=_G.OldCF
game.Players.LocalPlayer.Character=oldchar
end
_G.ClickFling=false -- Set this to true if u want.
loadstring(game:HttpGet(('https://raw.githubusercontent.com/XeneonPlays/Nexo/main/NexoPD'),true))()

IT = Instance.new
CF = CFrame.new
VT = Vector3.new
RAD = math.rad
C3 = Color3.new
UD2 = UDim2.new
BRICKC = BrickColor.new
ANGLES = CFrame.Angles
EULER = CFrame.fromEulerAnglesXYZ
COS = math.cos
ACOS = math.acos
SIN = math.sin
ASIN = math.asin
ABS = math.abs
MRANDOM = math.random
FLOOR = math.floor

speed = 1
sine = 1
srv = game:GetService('RunService')

function hatset(yes,part,c1,c0,nm)
reanim[yes].Handle.AccessoryWeld.Part1=reanim[part]
reanim[yes].Handle.AccessoryWeld.C1=c1 or CFrame.new()
reanim[yes].Handle.AccessoryWeld.C0=c0 or CFrame.new()--3bbb322dad5929d0d4f25adcebf30aa5
if nm==true then
noplsmesh(yes)
end
end

--put the hat script converted below

reanim = game.Players.LocalPlayer.Character.CWExtra.NexoPD
RJ = reanim.HumanoidRootPart.RootJoint
RS = reanim.Torso['Right Shoulder']
LS = reanim.Torso['Left Shoulder']
RH = reanim.Torso['Right Hip']
LH = reanim.Torso['Left Hip']
Root = reanim.HumanoidRootPart
NECK = reanim.Torso.Neck
NECK.C0 = CF(0,1,0)*ANGLES(RAD(0),RAD(0),RAD(0))
NECK.C1 = CF(0,-0.5,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RJ.C1 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RJ.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RS.C1 = CF(-0.5,0.5,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LS.C1 = CF(0.5,0.5,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RH.C1 = CF(0,1,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LH.C1 = CF(0,1,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RH.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LH.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RS.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LS.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))

Mode='1'

mousechanger=game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(k)
if k == 'urkeybind' then-- first mode
Mode='1'
elseif k == 'urkeybind' then-- second mode
Mode='2'
elseif k == 'urkeybind' then-- third mode
Mode='3'
end
end)

coroutine.wrap(function()
while true do -- anim changer
if HumanDied then mousechanger:Disconnect() break end
sine = sine + speed
local rlegray = Ray.new(reanim["Right Leg"].Position + Vector3.new(0, 0.5, 0), Vector3.new(0, -2, 0))
local rlegpart, rlegendPoint = workspace:FindPartOnRay(rlegray, char)
local llegray = Ray.new(reanim["Left Leg"].Position + Vector3.new(0, 0.5, 0), Vector3.new(0, -2, 0))
local llegpart, llegendPoint = workspace:FindPartOnRay(llegray, char)
local rightvector = (Root.Velocity * Root.CFrame.rightVector).X + (Root.Velocity * Root.CFrame.rightVector).Z
local lookvector = (Root.Velocity * Root.CFrame.lookVector).X + (Root.Velocity * Root.CFrame.lookVector).Z
if lookvector > reanim.Humanoid.WalkSpeed then
lookvector = reanim.Humanoid.WalkSpeed
end
if lookvector < -reanim.Humanoid.WalkSpeed then
lookvector = -reanim.Humanoid.WalkSpeed
end
if rightvector > reanim.Humanoid.WalkSpeed then
rightvector = reanim.Humanoid.WalkSpeed
end
if rightvector < -reanim.Humanoid.WalkSpeed then
rightvector = -reanim.Humanoid.WalkSpeed
end
local lookvel = lookvector / reanim.Humanoid.WalkSpeed
local rightvel = rightvector / reanim.Humanoid.WalkSpeed
if Mode == '1' then
if Root.Velocity.y > 1 then -- jump
    hatset('PlaidWrapHat','Torso',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),-1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-20+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+0999999999*math.cos(sine/13)),RAD(-66+0*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+999*math.cos(sine/13)),RAD(0+99*math.cos(sine/13)),RAD(0+9999*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+9999*math.cos(sine/13)),RAD(0+999*math.cos(sine/13)),RAD(0+99999*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+999999*math.cos(sine/13)),RAD(0+99999*math.cos(sine/13)),RAD(0+9999*math.cos(sine/13))),.3)
    
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
elseif Root.Velocity.y < -1 then -- fall
    hatset('PlaidWrapHat','Torso',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),-1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-20+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+0999999999*math.cos(sine/13)),RAD(-66+0*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+999*math.cos(sine/13)),RAD(0+99*math.cos(sine/13)),RAD(0+9999*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+9999*math.cos(sine/13)),RAD(0+999*math.cos(sine/13)),RAD(0+99999*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+999999*math.cos(sine/13)),RAD(0+99999*math.cos(sine/13)),RAD(0+9999*math.cos(sine/13))),.3)
    
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
elseif Root.Velocity.Magnitude < 2 then -- idle
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('PlaidWrapHat','Right Leg',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0.5+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),-2+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+0*math.cos(sine/13)),RAD(-66+0*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0.5+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),-2+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
elseif Root.Velocity.Magnitude < 20 then -- walk
    hatset('PlaidWrapHat','Torso',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-20+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+15*math.cos(sine/13)),RAD(-66+20*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+-0.1*math.cos(sine/13),0+-0.5*math.cos(sine/13))*ANGLES(RAD(0+50*math.cos(sine/13)),RAD(0+-50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+30*math.cos(sine/13)),RAD(0+30*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+-30*math.cos(sine/13)),RAD(0+-50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
elseif Root.Velocity.Magnitude > 20 then -- run
    hatset('PlaidWrapHat','Torso',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-20+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+15*math.cos(sine/13)),RAD(-66+20*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+-0.1*math.cos(sine/13),0+-0.5*math.cos(sine/13))*ANGLES(RAD(0+50*math.cos(sine/13)),RAD(0+-50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+30*math.cos(sine/13)),RAD(0+30*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+-30*math.cos(sine/13)),RAD(0+-50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
end
elseif Mode == '2' then
if Root.Velocity.y > 1 then -- jump
    hatset('PlaidWrapHat','Torso',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),-1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-20+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+0999999999*math.cos(sine/13)),RAD(-66+0*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+999*math.cos(sine/13)),RAD(0+99*math.cos(sine/13)),RAD(0+9999*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+9999*math.cos(sine/13)),RAD(0+999*math.cos(sine/13)),RAD(0+99999*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+999999*math.cos(sine/13)),RAD(0+99999*math.cos(sine/13)),RAD(0+9999*math.cos(sine/13))),.3)
    
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
elseif Root.Velocity.y < -1 then -- fall
    hatset('PlaidWrapHat','Torso',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),-1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-20+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+0999999999*math.cos(sine/13)),RAD(-66+0*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+999*math.cos(sine/13)),RAD(0+99*math.cos(sine/13)),RAD(0+9999*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+9999*math.cos(sine/13)),RAD(0+999*math.cos(sine/13)),RAD(0+99999*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+999999*math.cos(sine/13)),RAD(0+99999*math.cos(sine/13)),RAD(0+9999*math.cos(sine/13))),.3)
    
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
elseif Root.Velocity.Magnitude < 2 then -- idle
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('PlaidWrapHat','Right Leg',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0.5+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),-2+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+0*math.cos(sine/13)),RAD(-66+0*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0.5+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),-2+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
elseif Root.Velocity.Magnitude < 20 then -- walk
    hatset('PlaidWrapHat','Torso',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-20+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+15*math.cos(sine/13)),RAD(-66+20*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+-0.1*math.cos(sine/13),0+-0.5*math.cos(sine/13))*ANGLES(RAD(0+50*math.cos(sine/13)),RAD(0+-50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+30*math.cos(sine/13)),RAD(0+30*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+-30*math.cos(sine/13)),RAD(0+-50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
elseif Root.Velocity.Magnitude > 20 then -- run
    hatset('PlaidWrapHat','Torso',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-20+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+15*math.cos(sine/13)),RAD(-66+20*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+-0.1*math.cos(sine/13),0+-0.5*math.cos(sine/13))*ANGLES(RAD(0+50*math.cos(sine/13)),RAD(0+-50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+30*math.cos(sine/13)),RAD(0+30*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+-30*math.cos(sine/13)),RAD(0+-50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
end
elseif Mode == '3' then
if Root.Velocity.y > 1 then -- jump
    hatset('PlaidWrapHat','Torso',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),-1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-20+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+0999999999*math.cos(sine/13)),RAD(-66+0*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+999*math.cos(sine/13)),RAD(0+99*math.cos(sine/13)),RAD(0+9999*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+9999*math.cos(sine/13)),RAD(0+999*math.cos(sine/13)),RAD(0+99999*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+999999*math.cos(sine/13)),RAD(0+99999*math.cos(sine/13)),RAD(0+9999*math.cos(sine/13))),.3)
    
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
elseif Root.Velocity.y < -1 then -- fall
    hatset('PlaidWrapHat','Torso',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),-1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-20+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+0999999999*math.cos(sine/13)),RAD(-66+0*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+999*math.cos(sine/13)),RAD(0+99*math.cos(sine/13)),RAD(0+9999*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+9999*math.cos(sine/13)),RAD(0+999*math.cos(sine/13)),RAD(0+99999*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+999999*math.cos(sine/13)),RAD(0+99999*math.cos(sine/13)),RAD(0+9999*math.cos(sine/13))),.3)
    
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
elseif Root.Velocity.Magnitude < 2 then -- idle
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('PlaidWrapHat','Right Leg',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0.5+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),-2+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+0*math.cos(sine/13)),RAD(-66+0*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0.5+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),-2+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
elseif Root.Velocity.Magnitude < 20 then -- walk
    hatset('PlaidWrapHat','Torso',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-20+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+15*math.cos(sine/13)),RAD(-66+20*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+-0.1*math.cos(sine/13),0+-0.5*math.cos(sine/13))*ANGLES(RAD(0+50*math.cos(sine/13)),RAD(0+-50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+30*math.cos(sine/13)),RAD(0+30*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+-30*math.cos(sine/13)),RAD(0+-50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
elseif Root.Velocity.Magnitude > 20 then -- run
    hatset('PlaidWrapHat','Torso',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
    
    NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),0+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-20+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+15*math.cos(sine/13)),RAD(-66+20*math.cos(sine/13))),.3)
    LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+-0.1*math.cos(sine/13),0+-0.5*math.cos(sine/13))*ANGLES(RAD(0+50*math.cos(sine/13)),RAD(0+-50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+30*math.cos(sine/13)),RAD(0+30*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(20+-30*math.cos(sine/13)),RAD(0+-50*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    
    reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
    reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
end
end
srv.RenderStepped:Wait()
end
end)()
--Created using Nexo Animator




game.Players.LocalPlayer:GetMouse().Button1Down:Connect(function()
hatset('PlaidWrapHat','Torso',CFrame.new(),reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
hatset('MeshPartAccessory','Left Arm',CFrame.new(),reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)
hatset('WDW_FoamFinger','Torso',CFrame.new(),reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),1),true)

NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),0+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(67+0*math.cos(sine/13)),RAD(7+0*math.cos(sine/13)),RAD(-66+0*math.cos(sine/13))),.3)
LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+0.05*math.cos(sine/13),0+1*math.cos(sine/13))*ANGLES(RAD(85+-10*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(-5+-50*math.cos(sine/13))),.3)
RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(5+0*math.cos(sine/13))),.3)
LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0.05*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(5+0*math.cos(sine/13))),.3)

reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0 = reanim['PlaidWrapHat'].Handle.AccessoryWeld.C0:Lerp(CF(0+0*math.cos(sine/13),-0.1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(90+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0 = reanim['MeshPartAccessory'].Handle.AccessoryWeld.C0:Lerp(CF(0.01+0*math.cos(sine/13),0.1+0*math.cos(sine/13),0.000001+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0 = reanim['WDW_FoamFinger'].Handle.AccessoryWeld.C0:Lerp(CF(0+0.1*math.cos(sine/13),0.8+0.1*math.cos(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(25+20*math.cos(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.cos(sine/13))),.3)
end)
