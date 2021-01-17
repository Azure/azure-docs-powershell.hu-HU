---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: f2244bc1d0471924ad7f69ff600e70e92fdc809a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480310"
---
# <span data-ttu-id="617f0-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="617f0-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="617f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="617f0-102">SYNOPSIS</span></span>
<span data-ttu-id="617f0-103">Új szerepkör létrehozása egy eszközhöz</span><span class="sxs-lookup"><span data-stu-id="617f0-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="617f0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="617f0-104">SYNTAX</span></span>

### <span data-ttu-id="617f0-105">ConnectionStringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="617f0-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="617f0-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="617f0-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="617f0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="617f0-107">DESCRIPTION</span></span>
<span data-ttu-id="617f0-108">A **New-AzStackEdgeRole** parancsmag új szerepkört hoz létre a Stack Edge-hez.</span><span class="sxs-lookup"><span data-stu-id="617f0-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="617f0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="617f0-109">EXAMPLES</span></span>

### <span data-ttu-id="617f0-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="617f0-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="617f0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="617f0-111">PARAMETERS</span></span>

### <span data-ttu-id="617f0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="617f0-112">-AsJob</span></span>
<span data-ttu-id="617f0-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="617f0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="617f0-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="617f0-114">-ConnectionString</span></span>
<span data-ttu-id="617f0-115">Kapcsolati karakterláncok biztosítanak</span><span class="sxs-lookup"><span data-stu-id="617f0-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="617f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="617f0-116">-DefaultProfile</span></span>
<span data-ttu-id="617f0-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="617f0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="617f0-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="617f0-118">-DeviceName</span></span>
<span data-ttu-id="617f0-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="617f0-119">Device Name</span></span>

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

### <span data-ttu-id="617f0-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="617f0-120">-DeviceProperty</span></span>
<span data-ttu-id="617f0-121">Eszköztulajdonságok beállítása</span><span class="sxs-lookup"><span data-stu-id="617f0-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="617f0-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="617f0-122">-EncryptionKey</span></span>
<span data-ttu-id="617f0-123">A Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="617f0-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="617f0-124">-iotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="617f0-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="617f0-125">Iot Device Access Key</span><span class="sxs-lookup"><span data-stu-id="617f0-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="617f0-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="617f0-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="617f0-127">Adja meg az IOT-eszköz kapcsolati karakterláncát</span><span class="sxs-lookup"><span data-stu-id="617f0-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="617f0-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="617f0-128">-IotDeviceId</span></span>
<span data-ttu-id="617f0-129">Az iot-eszköz eszközazonosítója</span><span class="sxs-lookup"><span data-stu-id="617f0-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="617f0-130">-iotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="617f0-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="617f0-131">Az Iot Edge-eszköz hozzáférési kulcsa</span><span class="sxs-lookup"><span data-stu-id="617f0-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="617f0-132">-iotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="617f0-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="617f0-133">Adja meg a Edge-eszköz kapcsolati karakterláncát</span><span class="sxs-lookup"><span data-stu-id="617f0-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="617f0-134">-iotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="617f0-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="617f0-135">Az Iot Edge-eszköz azonosítója</span><span class="sxs-lookup"><span data-stu-id="617f0-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="617f0-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="617f0-136">-IotHostHub</span></span>
<span data-ttu-id="617f0-137">Hosthub-cím</span><span class="sxs-lookup"><span data-stu-id="617f0-137">Hosthub address</span></span>

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

### <span data-ttu-id="617f0-138">-Name</span><span class="sxs-lookup"><span data-stu-id="617f0-138">-Name</span></span>
<span data-ttu-id="617f0-139">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="617f0-139">Resource Name</span></span>

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

### <span data-ttu-id="617f0-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="617f0-140">-Platform</span></span>
<span data-ttu-id="617f0-141">Platform biztosítanak például: Linux</span><span class="sxs-lookup"><span data-stu-id="617f0-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="617f0-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="617f0-142">-ResourceGroupName</span></span>
<span data-ttu-id="617f0-143">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="617f0-143">Resource Group Name</span></span>

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

### <span data-ttu-id="617f0-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="617f0-144">-RoleStatus</span></span>
<span data-ttu-id="617f0-145">Az állapot engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="617f0-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="617f0-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="617f0-146">-Confirm</span></span>
<span data-ttu-id="617f0-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="617f0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="617f0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="617f0-148">-WhatIf</span></span>
<span data-ttu-id="617f0-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="617f0-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="617f0-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="617f0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="617f0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="617f0-151">CommonParameters</span></span>
<span data-ttu-id="617f0-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="617f0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="617f0-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="617f0-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="617f0-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="617f0-154">INPUTS</span></span>

### <span data-ttu-id="617f0-155">Nincs</span><span class="sxs-lookup"><span data-stu-id="617f0-155">None</span></span>

## <span data-ttu-id="617f0-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="617f0-156">OUTPUTS</span></span>

### <span data-ttu-id="617f0-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="617f0-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="617f0-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="617f0-158">NOTES</span></span>

## <span data-ttu-id="617f0-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="617f0-159">RELATED LINKS</span></span>
