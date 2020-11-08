---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8418A93-8E6B-4A1C-B319-7CACE95AB600
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1daf0cb8881beeb71f0b3fe68732d596c56ce12
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016240"
---
# <span data-ttu-id="3df62-101">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="3df62-101">Move-AzureService</span></span>

## <span data-ttu-id="3df62-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3df62-102">SYNOPSIS</span></span>
<span data-ttu-id="3df62-103">Felhőalapú szolgáltatás áttelepítése az Azure Resource Manager-kötegbe.</span><span class="sxs-lookup"><span data-stu-id="3df62-103">Migrates a cloud service to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="3df62-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3df62-104">SYNTAX</span></span>

### <span data-ttu-id="3df62-105">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="3df62-105">AbortMigrationParameterSet</span></span>
```
Move-AzureService [-Abort] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3df62-106">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="3df62-106">CommitMigrationParameterSet</span></span>
```
Move-AzureService [-Commit] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3df62-107">PrepareNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="3df62-107">PrepareNewMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3df62-108">PrepareExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="3df62-108">PrepareExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3df62-109">ValidateNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="3df62-109">ValidateNewMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3df62-110">ValidateExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="3df62-110">ValidateExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="3df62-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="3df62-111">DESCRIPTION</span></span>
<span data-ttu-id="3df62-112">A **Move-AzureService** parancsmag egy felhőalapú szolgáltatást és egy, a szolgáltatáson belüli központi üzembe helyezést áttelepít az Azure Resource Manager halom erőforrás csoportjába.</span><span class="sxs-lookup"><span data-stu-id="3df62-112">The **Move-AzureService** cmdlet migrates a cloud service and a deployment inside that service to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="3df62-113">Példák</span><span class="sxs-lookup"><span data-stu-id="3df62-113">EXAMPLES</span></span>

### <span data-ttu-id="3df62-114">1. példa: a szolgáltatás áttelepítésének előkészítése</span><span class="sxs-lookup"><span data-stu-id="3df62-114">Example 1: Prepare service migration</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="3df62-115">A parancs elkészíti a ContosoService nevű szolgáltatást az Azure Resource Manager-kötegbe való áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="3df62-115">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="3df62-116">Az áttelepítés tartalmazza a ContosoVM nevű központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="3df62-116">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="3df62-117">2. példa: a szolgáltatás áttelepítésének megkezdése</span><span class="sxs-lookup"><span data-stu-id="3df62-117">Example 2: Start service migration</span></span>
```
PS C:\> Move-AzureService -Commit -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="3df62-118">Ez a parancs elindítja a ContosoService nevű szolgáltatás áttelepítését az Azure Resource Manager-kötegbe.</span><span class="sxs-lookup"><span data-stu-id="3df62-118">This command starts migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="3df62-119">Az áttelepítés tartalmazza a ContosoVM nevű központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="3df62-119">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="3df62-120">3. példa: a szolgáltatás áttelepítésének visszavonása</span><span class="sxs-lookup"><span data-stu-id="3df62-120">Example 3: Cancel service migration</span></span>
```
PS C:\> Move-AzureService -Abort -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="3df62-121">Ez a parancs törli a ContosoService nevű szolgáltatás áttelepítését az Azure Resource Manager-kötegbe.</span><span class="sxs-lookup"><span data-stu-id="3df62-121">This command cancels migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="3df62-122">4. példa: a szolgáltatás áttelepítésének előkészítése meglévő virtuális hálózatra</span><span class="sxs-lookup"><span data-stu-id="3df62-122">Example 4: Prepare service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "VnetRG" -VirtualNetworkName "ContosoVNET" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="3df62-123">A parancs elkészíti a ContosoService nevű szolgáltatást az Azure Resource Manager-kötegbe való áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="3df62-123">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="3df62-124">Az áttelepítés tartalmazza a ContosoVM nevű központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="3df62-124">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="3df62-125">Az áttelepítés a korábban létrehozott virtuális hálózatot használja.</span><span class="sxs-lookup"><span data-stu-id="3df62-125">The migration uses a virtual network that was previously created.</span></span>

### <span data-ttu-id="3df62-126">5. példa: a szolgáltatás áttelepítésének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="3df62-126">Example 5: Validate service migration</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="3df62-127">Ez a parancs ellenőrzi a ContosoService nevű szolgáltatás áttelepítését az Azure Resource Manager-kötegbe.</span><span class="sxs-lookup"><span data-stu-id="3df62-127">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="3df62-128">Az áttelepítés tartalmazza a ContosoVM nevű központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="3df62-128">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="3df62-129">Példa 6: a szolgáltatás áttelepítése meglévő virtuális hálózatba</span><span class="sxs-lookup"><span data-stu-id="3df62-129">Example 6: Validate service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "contosoService" -DeploymentName "contosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "vnetRG" -VirtualNetworkName "contosoVNET" -SubnetName "contosoSubnet"
```

<span data-ttu-id="3df62-130">Ez a parancs ellenőrzi a ContosoService nevű szolgáltatás áttelepítését az Azure Resource Manager-kötegbe.</span><span class="sxs-lookup"><span data-stu-id="3df62-130">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="3df62-131">Az áttelepítés tartalmazza a ContosoVM nevű központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="3df62-131">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="3df62-132">Az áttelepítés a korábban létrehozott virtuális hálózatot használja.</span><span class="sxs-lookup"><span data-stu-id="3df62-132">The migration uses a virtual network that was previously created.</span></span>

## <span data-ttu-id="3df62-133">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3df62-133">PARAMETERS</span></span>

### <span data-ttu-id="3df62-134">-Megszakítás</span><span class="sxs-lookup"><span data-stu-id="3df62-134">-Abort</span></span>
<span data-ttu-id="3df62-135">Jelzi, hogy ez a parancsmag lemondja a szolgáltatás áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="3df62-135">Indicates that this cmdlet cancels the service migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df62-136">-Commit</span><span class="sxs-lookup"><span data-stu-id="3df62-136">-Commit</span></span>
<span data-ttu-id="3df62-137">Azt jelzi, hogy ez a parancsmag elindítja a szolgáltatás áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="3df62-137">Indicates that this cmdlet starts the service migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df62-138">-CreateNewVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3df62-138">-CreateNewVirtualNetwork</span></span>
<span data-ttu-id="3df62-139">Jelzi, hogy ez a parancsmag virtuális hálózatot hoz létre az Azure Resource Manager-kötegben.</span><span class="sxs-lookup"><span data-stu-id="3df62-139">Indicates that this cmdlet creates a virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, ValidateNewMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df62-140">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="3df62-140">-DeploymentName</span></span>
<span data-ttu-id="3df62-141">Annak a Felhőbeli szolgáltatásnak a nevét adja meg, amelyre a parancsmag át van telepítve.</span><span class="sxs-lookup"><span data-stu-id="3df62-141">Specifies the name of the cloud service deployment that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df62-142">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3df62-142">-InformationAction</span></span>
<span data-ttu-id="3df62-143">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="3df62-143">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3df62-144">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3df62-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3df62-145">Folytassa</span><span class="sxs-lookup"><span data-stu-id="3df62-145">Continue</span></span>
- <span data-ttu-id="3df62-146">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="3df62-146">Ignore</span></span>
- <span data-ttu-id="3df62-147">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="3df62-147">Inquire</span></span>
- <span data-ttu-id="3df62-148">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3df62-148">SilentlyContinue</span></span>
- <span data-ttu-id="3df62-149">állj</span><span class="sxs-lookup"><span data-stu-id="3df62-149">Stop</span></span>
- <span data-ttu-id="3df62-150">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="3df62-150">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df62-151">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3df62-151">-InformationVariable</span></span>
<span data-ttu-id="3df62-152">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="3df62-152">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df62-153">– Előkészületek</span><span class="sxs-lookup"><span data-stu-id="3df62-153">-Prepare</span></span>
<span data-ttu-id="3df62-154">Jelzi, hogy ez a parancsmag előkészíti a felhőalapú szolgáltatást az áttelepítésre.</span><span class="sxs-lookup"><span data-stu-id="3df62-154">Indicates that this cmdlet prepares the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, PrepareExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df62-155">-Profil</span><span class="sxs-lookup"><span data-stu-id="3df62-155">-Profile</span></span>
<span data-ttu-id="3df62-156">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3df62-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3df62-157">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3df62-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df62-158">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="3df62-158">-ServiceName</span></span>
<span data-ttu-id="3df62-159">Annak a Felhőbeli szolgáltatásnak a nevét adja meg, amelyre a parancsmag át van telepítve.</span><span class="sxs-lookup"><span data-stu-id="3df62-159">Specifies the name  of the cloud service that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3df62-160">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3df62-160">-SubnetName</span></span>
<span data-ttu-id="3df62-161">A virtuális hálózaton belüli alhálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3df62-161">Specifies the name of the Subnet inside the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df62-162">-UseExistingVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3df62-162">-UseExistingVirtualNetwork</span></span>
<span data-ttu-id="3df62-163">Jelzi, hogy ez a parancsmag áttelepíti a felhőalapú szolgáltatást egy meglévő virtuális hálózatra az Azure Resource Manager-kötegben.</span><span class="sxs-lookup"><span data-stu-id="3df62-163">Indicates that this cmdlet migrates the cloud service to an existing virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df62-164">– Érvényesítés</span><span class="sxs-lookup"><span data-stu-id="3df62-164">-Validate</span></span>
<span data-ttu-id="3df62-165">Azt adja meg, hogy ez a parancsmag ellenőrzi-e a felhőalapú szolgáltatást az áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="3df62-165">Specifies that this cmdlet validates the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateNewMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df62-166">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3df62-166">-VirtualNetworkName</span></span>
<span data-ttu-id="3df62-167">A virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3df62-167">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df62-168">-VirtualNetworkResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df62-168">-VirtualNetworkResourceGroupName</span></span>
<span data-ttu-id="3df62-169">Egy meglévő virtuális hálózat erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3df62-169">Specifies the name of the resource group of an existing virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df62-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df62-170">CommonParameters</span></span>
<span data-ttu-id="3df62-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3df62-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df62-172">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3df62-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df62-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3df62-173">INPUTS</span></span>

## <span data-ttu-id="3df62-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3df62-174">OUTPUTS</span></span>

## <span data-ttu-id="3df62-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3df62-175">NOTES</span></span>

## <span data-ttu-id="3df62-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3df62-176">RELATED LINKS</span></span>

[<span data-ttu-id="3df62-177">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3df62-177">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="3df62-178">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="3df62-178">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="3df62-179">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="3df62-179">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="3df62-180">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3df62-180">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="3df62-181">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3df62-181">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


