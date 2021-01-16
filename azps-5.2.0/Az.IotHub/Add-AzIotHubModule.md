---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
ms.openlocfilehash: 44e6451542a75e97a57890261a9a5f312e5ec466
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345222"
---
# <span data-ttu-id="9ff09-101">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="9ff09-101">Add-AzIotHubModule</span></span>

## <span data-ttu-id="9ff09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ff09-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff09-103">Hozzon létre egy modult egy cél IoT-eszközön egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="9ff09-103">Create a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="9ff09-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9ff09-104">SYNTAX</span></span>

### <span data-ttu-id="9ff09-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9ff09-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ff09-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9ff09-106">InputObjectSet</span></span>
```
Add-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ff09-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9ff09-107">ResourceIdSet</span></span>
```
Add-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ff09-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9ff09-108">DESCRIPTION</span></span>
<span data-ttu-id="9ff09-109">Hozzon létre egy modult egy másik engedélyezési típussal egy IoT-központban egy céleszközön.</span><span class="sxs-lookup"><span data-stu-id="9ff09-109">Create a module on a target IoT device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="9ff09-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9ff09-110">EXAMPLES</span></span>

### <span data-ttu-id="9ff09-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="9ff09-111">Example 1</span></span>
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

<span data-ttu-id="9ff09-112">Hozzon létre egy modult egy alapértelmezett engedélyezési eszközzel (megosztott privát kulcs).</span><span class="sxs-lookup"><span data-stu-id="9ff09-112">Create a module on a target IoT device with default authorization (shared private key).</span></span>

## <span data-ttu-id="9ff09-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ff09-113">PARAMETERS</span></span>

### <span data-ttu-id="9ff09-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="9ff09-114">-AuthMethod</span></span>
<span data-ttu-id="9ff09-115">Az engedélyezési típus, amely alapján egy entitást létre kell hozatni.</span><span class="sxs-lookup"><span data-stu-id="9ff09-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="9ff09-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff09-116">-DefaultProfile</span></span>
<span data-ttu-id="9ff09-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ff09-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ff09-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9ff09-118">-DeviceId</span></span>
<span data-ttu-id="9ff09-119">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9ff09-119">Target Device Id.</span></span>

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

### <span data-ttu-id="9ff09-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ff09-120">-InputObject</span></span>
<span data-ttu-id="9ff09-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="9ff09-121">IotHub object</span></span>

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

### <span data-ttu-id="9ff09-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9ff09-122">-IotHubName</span></span>
<span data-ttu-id="9ff09-123">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="9ff09-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9ff09-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="9ff09-124">-ModuleId</span></span>
<span data-ttu-id="9ff09-125">Célmodul-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9ff09-125">Target Module Id.</span></span>

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

### <span data-ttu-id="9ff09-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="9ff09-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="9ff09-127">Az elsődleges kulcshoz használható explicit öna aláírt tanúsítvány thumbprint.</span><span class="sxs-lookup"><span data-stu-id="9ff09-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="9ff09-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ff09-128">-ResourceGroupName</span></span>
<span data-ttu-id="9ff09-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9ff09-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9ff09-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ff09-130">-ResourceId</span></span>
<span data-ttu-id="9ff09-131">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="9ff09-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9ff09-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="9ff09-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="9ff09-133">Explicit öna aláírt tanúsítvány thumbprint for use for secondary key.</span><span class="sxs-lookup"><span data-stu-id="9ff09-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="9ff09-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ff09-134">-Confirm</span></span>
<span data-ttu-id="9ff09-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9ff09-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ff09-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ff09-136">-WhatIf</span></span>
<span data-ttu-id="9ff09-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9ff09-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ff09-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ff09-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ff09-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff09-139">CommonParameters</span></span>
<span data-ttu-id="9ff09-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff09-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff09-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ff09-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff09-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ff09-142">INPUTS</span></span>

### <span data-ttu-id="9ff09-143">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9ff09-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9ff09-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9ff09-144">System.String</span></span>

## <span data-ttu-id="9ff09-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ff09-145">OUTPUTS</span></span>

### <span data-ttu-id="9ff09-146">Microsoft.Azure.Commands.Management.iotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="9ff09-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="9ff09-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9ff09-147">NOTES</span></span>

## <span data-ttu-id="9ff09-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ff09-148">RELATED LINKS</span></span>