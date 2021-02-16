---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: aa44399adcfd5e39d956215b7ca824e5ef9abd60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204503"
---
# <span data-ttu-id="edbe6-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="edbe6-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="edbe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edbe6-102">SYNOPSIS</span></span>
<span data-ttu-id="edbe6-103">Új szerepkör létrehozása egy eszközhöz</span><span class="sxs-lookup"><span data-stu-id="edbe6-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="edbe6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="edbe6-104">SYNTAX</span></span>

### <span data-ttu-id="edbe6-105">ConnectionStringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="edbe6-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edbe6-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="edbe6-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edbe6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="edbe6-107">DESCRIPTION</span></span>
<span data-ttu-id="edbe6-108">A **New-AzDataBoxEdgeRole** parancsmag új szerepkört hoz létre egy Data Box Edge-eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="edbe6-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="edbe6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="edbe6-109">EXAMPLES</span></span>

### <span data-ttu-id="edbe6-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="edbe6-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="edbe6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edbe6-111">PARAMETERS</span></span>

### <span data-ttu-id="edbe6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edbe6-112">-AsJob</span></span>
<span data-ttu-id="edbe6-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="edbe6-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="edbe6-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="edbe6-114">-ConnectionString</span></span>
<span data-ttu-id="edbe6-115">Kapcsolati karakterláncok biztosítanak</span><span class="sxs-lookup"><span data-stu-id="edbe6-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="edbe6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edbe6-116">-DefaultProfile</span></span>
<span data-ttu-id="edbe6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="edbe6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edbe6-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="edbe6-118">-DeviceName</span></span>
<span data-ttu-id="edbe6-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="edbe6-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbe6-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="edbe6-120">-DeviceProperty</span></span>
<span data-ttu-id="edbe6-121">Eszköztulajdonságok beállítása</span><span class="sxs-lookup"><span data-stu-id="edbe6-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="edbe6-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="edbe6-122">-EncryptionKey</span></span>
<span data-ttu-id="edbe6-123">A Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="edbe6-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="edbe6-124">-iotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="edbe6-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="edbe6-125">Iot Device Access Key</span><span class="sxs-lookup"><span data-stu-id="edbe6-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="edbe6-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="edbe6-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="edbe6-127">Adja meg az IOT-eszköz kapcsolati karakterláncát</span><span class="sxs-lookup"><span data-stu-id="edbe6-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="edbe6-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="edbe6-128">-IotDeviceId</span></span>
<span data-ttu-id="edbe6-129">Az IOT-eszköz eszközazonosítója</span><span class="sxs-lookup"><span data-stu-id="edbe6-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="edbe6-130">-iotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="edbe6-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="edbe6-131">Az Iot Edge-eszköz hozzáférési kulcsa</span><span class="sxs-lookup"><span data-stu-id="edbe6-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="edbe6-132">-iotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="edbe6-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="edbe6-133">Adja meg a Edge-eszköz kapcsolati karakterláncát</span><span class="sxs-lookup"><span data-stu-id="edbe6-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="edbe6-134">-iotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="edbe6-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="edbe6-135">Az Iot Edge-eszköz azonosítója</span><span class="sxs-lookup"><span data-stu-id="edbe6-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="edbe6-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="edbe6-136">-IotHostHub</span></span>
<span data-ttu-id="edbe6-137">Hosthub-cím</span><span class="sxs-lookup"><span data-stu-id="edbe6-137">Hosthub address</span></span>

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

### <span data-ttu-id="edbe6-138">-Name</span><span class="sxs-lookup"><span data-stu-id="edbe6-138">-Name</span></span>
<span data-ttu-id="edbe6-139">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="edbe6-139">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbe6-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="edbe6-140">-Platform</span></span>
<span data-ttu-id="edbe6-141">Platform biztosítanak például: Linux</span><span class="sxs-lookup"><span data-stu-id="edbe6-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="edbe6-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edbe6-142">-ResourceGroupName</span></span>
<span data-ttu-id="edbe6-143">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="edbe6-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbe6-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="edbe6-144">-RoleStatus</span></span>
<span data-ttu-id="edbe6-145">Az állapot engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="edbe6-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="edbe6-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edbe6-146">-Confirm</span></span>
<span data-ttu-id="edbe6-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="edbe6-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edbe6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edbe6-148">-WhatIf</span></span>
<span data-ttu-id="edbe6-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="edbe6-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edbe6-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="edbe6-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edbe6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edbe6-151">CommonParameters</span></span>
<span data-ttu-id="edbe6-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edbe6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edbe6-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edbe6-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edbe6-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="edbe6-154">INPUTS</span></span>

### <span data-ttu-id="edbe6-155">Nincs</span><span class="sxs-lookup"><span data-stu-id="edbe6-155">None</span></span>

## <span data-ttu-id="edbe6-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="edbe6-156">OUTPUTS</span></span>

### <span data-ttu-id="edbe6-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="edbe6-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="edbe6-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="edbe6-158">NOTES</span></span>

## <span data-ttu-id="edbe6-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="edbe6-159">RELATED LINKS</span></span>
