---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
ms.openlocfilehash: 44e6451542a75e97a57890261a9a5f312e5ec466
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167378"
---
# <span data-ttu-id="b0f85-101">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="b0f85-101">Add-AzIotHubModule</span></span>

## <span data-ttu-id="b0f85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0f85-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f85-103">Hozzon létre egy modult egy cél IoT-eszközön egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="b0f85-103">Create a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="b0f85-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0f85-104">SYNTAX</span></span>

### <span data-ttu-id="b0f85-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0f85-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0f85-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b0f85-106">InputObjectSet</span></span>
```
Add-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0f85-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b0f85-107">ResourceIdSet</span></span>
```
Add-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0f85-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0f85-108">DESCRIPTION</span></span>
<span data-ttu-id="b0f85-109">Hozzon létre egy modult egy másik engedélyezési típust tároló cél IoT-eszközön az IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="b0f85-109">Create a module on a target IoT device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="b0f85-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0f85-110">EXAMPLES</span></span>

### <span data-ttu-id="b0f85-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="b0f85-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod shared_private_key

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  : 
```

<span data-ttu-id="b0f85-112">Hozzon létre egy modult egy alapértelmezett engedélyezési eszközzel (megosztott privát kulcs).</span><span class="sxs-lookup"><span data-stu-id="b0f85-112">Create a module on a target IoT device with default authorization (shared private key).</span></span>

## <span data-ttu-id="b0f85-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0f85-113">PARAMETERS</span></span>

### <span data-ttu-id="b0f85-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="b0f85-114">-AuthMethod</span></span>
<span data-ttu-id="b0f85-115">Az engedélyezési típus, amely alapján egy entitást létre kell hozatni.</span><span class="sxs-lookup"><span data-stu-id="b0f85-115">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0f85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f85-116">-DefaultProfile</span></span>
<span data-ttu-id="b0f85-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0f85-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0f85-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b0f85-118">-DeviceId</span></span>
<span data-ttu-id="b0f85-119">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b0f85-119">Target Device Id.</span></span>

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

### <span data-ttu-id="b0f85-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0f85-120">-InputObject</span></span>
<span data-ttu-id="b0f85-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="b0f85-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f85-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b0f85-122">-IotHubName</span></span>
<span data-ttu-id="b0f85-123">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="b0f85-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0f85-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="b0f85-124">-ModuleId</span></span>
<span data-ttu-id="b0f85-125">Célmodul-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b0f85-125">Target Module Id.</span></span>

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

### <span data-ttu-id="b0f85-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="b0f85-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="b0f85-127">Explicit öna aláírt tanúsítvány thumbprint for use for primary key.</span><span class="sxs-lookup"><span data-stu-id="b0f85-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="b0f85-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0f85-128">-ResourceGroupName</span></span>
<span data-ttu-id="b0f85-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b0f85-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0f85-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0f85-130">-ResourceId</span></span>
<span data-ttu-id="b0f85-131">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b0f85-131">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f85-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="b0f85-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="b0f85-133">Explicit öna aláírt tanúsítvány thumbprint for use for secondary key.</span><span class="sxs-lookup"><span data-stu-id="b0f85-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0f85-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0f85-134">-Confirm</span></span>
<span data-ttu-id="b0f85-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b0f85-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0f85-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0f85-136">-WhatIf</span></span>
<span data-ttu-id="b0f85-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b0f85-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0f85-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0f85-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0f85-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f85-139">CommonParameters</span></span>
<span data-ttu-id="b0f85-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0f85-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f85-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0f85-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f85-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0f85-142">INPUTS</span></span>

### <span data-ttu-id="b0f85-143">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b0f85-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b0f85-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b0f85-144">System.String</span></span>

## <span data-ttu-id="b0f85-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0f85-145">OUTPUTS</span></span>

### <span data-ttu-id="b0f85-146">Microsoft.Azure.Commands.Management.iotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="b0f85-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="b0f85-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0f85-147">NOTES</span></span>

## <span data-ttu-id="b0f85-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0f85-148">RELATED LINKS</span></span>