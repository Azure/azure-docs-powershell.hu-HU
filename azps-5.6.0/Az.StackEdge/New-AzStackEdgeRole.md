---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: 785c092333d0e083ed3ee356a0c4e76d6188b96b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005269"
---
# <span data-ttu-id="a53ca-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="a53ca-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="a53ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a53ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a53ca-103">Új szerepkör létrehozása egy eszközhöz</span><span class="sxs-lookup"><span data-stu-id="a53ca-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="a53ca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a53ca-104">SYNTAX</span></span>

### <span data-ttu-id="a53ca-105">ConnectionStringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a53ca-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a53ca-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="a53ca-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a53ca-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a53ca-107">DESCRIPTION</span></span>
<span data-ttu-id="a53ca-108">A **New-AzStackEdgeRole** parancsmag új szerepkört hoz létre a Stack Edge-hez.</span><span class="sxs-lookup"><span data-stu-id="a53ca-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="a53ca-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a53ca-109">EXAMPLES</span></span>

### <span data-ttu-id="a53ca-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="a53ca-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="a53ca-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a53ca-111">PARAMETERS</span></span>

### <span data-ttu-id="a53ca-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a53ca-112">-AsJob</span></span>
<span data-ttu-id="a53ca-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a53ca-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a53ca-114">-ConnectionString</span></span>
<span data-ttu-id="a53ca-115">Kapcsolati karakterláncok biztosítanak</span><span class="sxs-lookup"><span data-stu-id="a53ca-115">To Provide Connection Strings</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a53ca-116">-DefaultProfile</span></span>
<span data-ttu-id="a53ca-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a53ca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a53ca-118">-DeviceName</span></span>
<span data-ttu-id="a53ca-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="a53ca-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="a53ca-120">-DeviceProperty</span></span>
<span data-ttu-id="a53ca-121">Eszköztulajdonságok beállítása</span><span class="sxs-lookup"><span data-stu-id="a53ca-121">To Provide Device Properties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IotParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a53ca-122">-EncryptionKey</span></span>
<span data-ttu-id="a53ca-123">A Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="a53ca-123">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-124">-iotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="a53ca-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="a53ca-125">Iot Device Access Key</span><span class="sxs-lookup"><span data-stu-id="a53ca-125">Iot Device Access Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="a53ca-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="a53ca-127">Adja meg az IOT-eszköz kapcsolati karakterláncát</span><span class="sxs-lookup"><span data-stu-id="a53ca-127">Please provide connection string of IOT Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="a53ca-128">-IotDeviceId</span></span>
<span data-ttu-id="a53ca-129">Az iot-eszköz eszközazonosítója</span><span class="sxs-lookup"><span data-stu-id="a53ca-129">Device Id of the Iot Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-130">-iotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="a53ca-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="a53ca-131">Az Iot Edge-eszköz hozzáférési kulcsa</span><span class="sxs-lookup"><span data-stu-id="a53ca-131">Access key of the Iot Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="a53ca-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="a53ca-133">Adja meg a Edge-eszköz kapcsolati karakterláncát</span><span class="sxs-lookup"><span data-stu-id="a53ca-133">Please provide connection string of Edge Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-134">-iotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="a53ca-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="a53ca-135">Az Iot Edge-eszköz azonosítója</span><span class="sxs-lookup"><span data-stu-id="a53ca-135">Id of the Iot Edge Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="a53ca-136">-IotHostHub</span></span>
<span data-ttu-id="a53ca-137">Hosthub-cím</span><span class="sxs-lookup"><span data-stu-id="a53ca-137">Hosthub address</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-138">-Name</span><span class="sxs-lookup"><span data-stu-id="a53ca-138">-Name</span></span>
<span data-ttu-id="a53ca-139">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="a53ca-139">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="a53ca-140">-Platform</span></span>
<span data-ttu-id="a53ca-141">Platform biztosítanak például: Linux</span><span class="sxs-lookup"><span data-stu-id="a53ca-141">Provide the Platform, for ex: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a53ca-142">-ResourceGroupName</span></span>
<span data-ttu-id="a53ca-143">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a53ca-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="a53ca-144">-RoleStatus</span></span>
<span data-ttu-id="a53ca-145">Az állapot engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="a53ca-145">Provide the status enable/disable</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a53ca-146">-Confirm</span></span>
<span data-ttu-id="a53ca-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a53ca-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a53ca-148">-WhatIf</span></span>
<span data-ttu-id="a53ca-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a53ca-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a53ca-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a53ca-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53ca-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a53ca-151">CommonParameters</span></span>
<span data-ttu-id="a53ca-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a53ca-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a53ca-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a53ca-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a53ca-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a53ca-154">INPUTS</span></span>

### <span data-ttu-id="a53ca-155">Nincs</span><span class="sxs-lookup"><span data-stu-id="a53ca-155">None</span></span>

## <span data-ttu-id="a53ca-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a53ca-156">OUTPUTS</span></span>

### <span data-ttu-id="a53ca-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="a53ca-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="a53ca-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a53ca-158">NOTES</span></span>

## <span data-ttu-id="a53ca-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a53ca-159">RELATED LINKS</span></span>
