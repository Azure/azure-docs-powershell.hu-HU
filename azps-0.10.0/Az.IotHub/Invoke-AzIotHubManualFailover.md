---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: 5055960ae541ef93d57eee53078413143fad7839
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843954"
---
# <span data-ttu-id="54e84-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="54e84-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="54e84-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54e84-102">SYNOPSIS</span></span>
<span data-ttu-id="54e84-103">A IoT-hub feladatátvételi folyamatának meghívása a Geo-párosított katasztrófa-helyreállítási területre.</span><span class="sxs-lookup"><span data-stu-id="54e84-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="54e84-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54e84-104">SYNTAX</span></span>

### <span data-ttu-id="54e84-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="54e84-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54e84-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="54e84-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54e84-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="54e84-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54e84-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="54e84-108">DESCRIPTION</span></span>
<span data-ttu-id="54e84-109">A IoT-hub feladatátvételét a másodlagos helyre fogja kezdeményezni.</span><span class="sxs-lookup"><span data-stu-id="54e84-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="54e84-110">Ez a műveletek lelassítják az időt, és telemetriai a megoldást.</span><span class="sxs-lookup"><span data-stu-id="54e84-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="54e84-111">Ez egy hosszú futási művelet, és néhány percet igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="54e84-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="54e84-112">Kérjük, körültekintően járjon el, amikor használja.</span><span class="sxs-lookup"><span data-stu-id="54e84-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="54e84-113">Példák</span><span class="sxs-lookup"><span data-stu-id="54e84-113">EXAMPLES</span></span>

### <span data-ttu-id="54e84-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="54e84-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="54e84-115">A "myiothub" IoT-hub feladatátvételi folyamatának kezdeményezése.</span><span class="sxs-lookup"><span data-stu-id="54e84-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="54e84-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="54e84-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="54e84-117">A "myiothub" IoT-hub feladatátvételi folyamatának kezdeményezése a háttérben.</span><span class="sxs-lookup"><span data-stu-id="54e84-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="54e84-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54e84-118">PARAMETERS</span></span>

### <span data-ttu-id="54e84-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54e84-119">-AsJob</span></span>
<span data-ttu-id="54e84-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="54e84-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54e84-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e84-121">-DefaultProfile</span></span>
<span data-ttu-id="54e84-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54e84-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54e84-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54e84-123">-InputObject</span></span>
<span data-ttu-id="54e84-124">IOT hub objektum</span><span class="sxs-lookup"><span data-stu-id="54e84-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="54e84-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="54e84-125">-Name</span></span>
<span data-ttu-id="54e84-126">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="54e84-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="54e84-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54e84-127">-PassThru</span></span>
<span data-ttu-id="54e84-128">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="54e84-128">Allows to return the boolean object.</span></span> <span data-ttu-id="54e84-129">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="54e84-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="54e84-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54e84-130">-ResourceGroupName</span></span>
<span data-ttu-id="54e84-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="54e84-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="54e84-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54e84-132">-ResourceId</span></span>
<span data-ttu-id="54e84-133">IOT hub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="54e84-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="54e84-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54e84-134">-Confirm</span></span>
<span data-ttu-id="54e84-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54e84-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54e84-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54e84-136">-WhatIf</span></span>
<span data-ttu-id="54e84-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54e84-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54e84-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54e84-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54e84-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e84-139">CommonParameters</span></span>
<span data-ttu-id="54e84-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54e84-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e84-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54e84-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e84-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54e84-142">INPUTS</span></span>

### <span data-ttu-id="54e84-143">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="54e84-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="54e84-144">System. String</span><span class="sxs-lookup"><span data-stu-id="54e84-144">System.String</span></span>

## <span data-ttu-id="54e84-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54e84-145">OUTPUTS</span></span>

### <span data-ttu-id="54e84-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54e84-146">System.Boolean</span></span>

## <span data-ttu-id="54e84-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54e84-147">NOTES</span></span>

## <span data-ttu-id="54e84-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54e84-148">RELATED LINKS</span></span>
