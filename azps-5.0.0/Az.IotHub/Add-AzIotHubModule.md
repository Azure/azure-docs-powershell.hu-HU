---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
ms.openlocfilehash: 44e6451542a75e97a57890261a9a5f312e5ec466
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187775"
---
# <span data-ttu-id="9ba3f-101">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="9ba3f-101">Add-AzIotHubModule</span></span>

## <span data-ttu-id="9ba3f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ba3f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba3f-103">Hozzon létre egy modult egy cél IoT-eszközön egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-103">Create a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="9ba3f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ba3f-104">SYNTAX</span></span>

### <span data-ttu-id="9ba3f-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9ba3f-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ba3f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9ba3f-106">InputObjectSet</span></span>
```
Add-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ba3f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9ba3f-107">ResourceIdSet</span></span>
```
Add-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ba3f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ba3f-108">DESCRIPTION</span></span>
<span data-ttu-id="9ba3f-109">Hozzon létre egy modult egy cél IoT-eszközön, amelyen a IoT-hub különböző engedélyezési típusú.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-109">Create a module on a target IoT device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="9ba3f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9ba3f-110">EXAMPLES</span></span>

### <span data-ttu-id="9ba3f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9ba3f-111">Example 1</span></span>
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

<span data-ttu-id="9ba3f-112">Hozzon létre egy modult egy cél IoT-eszközön alapértelmezett engedéllyel (megosztott titkos kulccsal).</span><span class="sxs-lookup"><span data-stu-id="9ba3f-112">Create a module on a target IoT device with default authorization (shared private key).</span></span>

## <span data-ttu-id="9ba3f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ba3f-113">PARAMETERS</span></span>

### <span data-ttu-id="9ba3f-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="9ba3f-114">-AuthMethod</span></span>
<span data-ttu-id="9ba3f-115">Az engedély típusa: egy entitást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="9ba3f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba3f-116">-DefaultProfile</span></span>
<span data-ttu-id="9ba3f-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ba3f-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9ba3f-118">-DeviceId</span></span>
<span data-ttu-id="9ba3f-119">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-119">Target Device Id.</span></span>

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

### <span data-ttu-id="9ba3f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ba3f-120">-InputObject</span></span>
<span data-ttu-id="9ba3f-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="9ba3f-121">IotHub object</span></span>

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

### <span data-ttu-id="9ba3f-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9ba3f-122">-IotHubName</span></span>
<span data-ttu-id="9ba3f-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="9ba3f-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9ba3f-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="9ba3f-124">-ModuleId</span></span>
<span data-ttu-id="9ba3f-125">A cél modul azonosítója</span><span class="sxs-lookup"><span data-stu-id="9ba3f-125">Target Module Id.</span></span>

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

### <span data-ttu-id="9ba3f-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="9ba3f-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="9ba3f-127">Explicit önaláírt tanúsítvány-ujjlenyomat az elsődleges kulcshoz való használathoz.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="9ba3f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba3f-128">-ResourceGroupName</span></span>
<span data-ttu-id="9ba3f-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9ba3f-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9ba3f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ba3f-130">-ResourceId</span></span>
<span data-ttu-id="9ba3f-131">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="9ba3f-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9ba3f-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="9ba3f-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="9ba3f-133">Explicit önaláírt tanúsítvány-ujjlenyomat a másodlagos kulcshoz való használathoz.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="9ba3f-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9ba3f-134">-Confirm</span></span>
<span data-ttu-id="9ba3f-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ba3f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ba3f-136">-WhatIf</span></span>
<span data-ttu-id="9ba3f-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ba3f-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ba3f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba3f-139">CommonParameters</span></span>
<span data-ttu-id="9ba3f-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ba3f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba3f-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ba3f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba3f-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ba3f-142">INPUTS</span></span>

### <span data-ttu-id="9ba3f-143">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9ba3f-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9ba3f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9ba3f-144">System.String</span></span>

## <span data-ttu-id="9ba3f-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ba3f-145">OUTPUTS</span></span>

### <span data-ttu-id="9ba3f-146">Microsoft. Azure. Command. Management. IotHub. models. PSModule</span><span class="sxs-lookup"><span data-stu-id="9ba3f-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="9ba3f-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ba3f-147">NOTES</span></span>

## <span data-ttu-id="9ba3f-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ba3f-148">RELATED LINKS</span></span>