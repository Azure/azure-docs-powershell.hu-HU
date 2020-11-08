---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195976"
---
# <span data-ttu-id="4e2d1-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="4e2d1-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="4e2d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e2d1-102">SYNOPSIS</span></span>
<span data-ttu-id="4e2d1-103">A IoT-hub feladatátvételi folyamatának meghívása a Geo-párosított katasztrófa-helyreállítási területre.</span><span class="sxs-lookup"><span data-stu-id="4e2d1-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="4e2d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e2d1-104">SYNTAX</span></span>

### <span data-ttu-id="4e2d1-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e2d1-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e2d1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4e2d1-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e2d1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4e2d1-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e2d1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e2d1-108">DESCRIPTION</span></span>
<span data-ttu-id="4e2d1-109">A IoT-hub feladatátvételét a másodlagos helyre fogja kezdeményezni.</span><span class="sxs-lookup"><span data-stu-id="4e2d1-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="4e2d1-110">Ez a műveletek lelassítják az időt, és telemetriai a megoldást.</span><span class="sxs-lookup"><span data-stu-id="4e2d1-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="4e2d1-111">Ez egy hosszú futási művelet, és néhány percet igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="4e2d1-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="4e2d1-112">Kérjük, körültekintően járjon el, amikor használja.</span><span class="sxs-lookup"><span data-stu-id="4e2d1-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="4e2d1-113">Példák</span><span class="sxs-lookup"><span data-stu-id="4e2d1-113">EXAMPLES</span></span>

### <span data-ttu-id="4e2d1-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4e2d1-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="4e2d1-115">A "myiothub" IoT-hub feladatátvételi folyamatának kezdeményezése.</span><span class="sxs-lookup"><span data-stu-id="4e2d1-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="4e2d1-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="4e2d1-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="4e2d1-117">A "myiothub" IoT-hub feladatátvételi folyamatának kezdeményezése a háttérben.</span><span class="sxs-lookup"><span data-stu-id="4e2d1-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="4e2d1-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e2d1-118">PARAMETERS</span></span>

### <span data-ttu-id="4e2d1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e2d1-119">-AsJob</span></span>
<span data-ttu-id="4e2d1-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4e2d1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e2d1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e2d1-121">-DefaultProfile</span></span>
<span data-ttu-id="4e2d1-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e2d1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e2d1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e2d1-123">-InputObject</span></span>
<span data-ttu-id="4e2d1-124">IOT hub objektum</span><span class="sxs-lookup"><span data-stu-id="4e2d1-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="4e2d1-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e2d1-125">-Name</span></span>
<span data-ttu-id="4e2d1-126">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="4e2d1-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4e2d1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e2d1-127">-PassThru</span></span>
<span data-ttu-id="4e2d1-128">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="4e2d1-128">Allows to return the boolean object.</span></span> <span data-ttu-id="4e2d1-129">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4e2d1-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4e2d1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e2d1-130">-ResourceGroupName</span></span>
<span data-ttu-id="4e2d1-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4e2d1-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4e2d1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e2d1-132">-ResourceId</span></span>
<span data-ttu-id="4e2d1-133">IOT hub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="4e2d1-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="4e2d1-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4e2d1-134">-Confirm</span></span>
<span data-ttu-id="4e2d1-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e2d1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e2d1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e2d1-136">-WhatIf</span></span>
<span data-ttu-id="4e2d1-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4e2d1-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e2d1-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e2d1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e2d1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e2d1-139">CommonParameters</span></span>
<span data-ttu-id="4e2d1-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e2d1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e2d1-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e2d1-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e2d1-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e2d1-142">INPUTS</span></span>

### <span data-ttu-id="4e2d1-143">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4e2d1-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4e2d1-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4e2d1-144">System.String</span></span>

## <span data-ttu-id="4e2d1-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e2d1-145">OUTPUTS</span></span>

### <span data-ttu-id="4e2d1-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4e2d1-146">System.Boolean</span></span>

## <span data-ttu-id="4e2d1-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e2d1-147">NOTES</span></span>

## <span data-ttu-id="4e2d1-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e2d1-148">RELATED LINKS</span></span>
