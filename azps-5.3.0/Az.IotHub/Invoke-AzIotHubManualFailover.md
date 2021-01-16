---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480230"
---
# <span data-ttu-id="6a4e1-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="6a4e1-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="6a4e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a4e1-102">SYNOPSIS</span></span>
<span data-ttu-id="6a4e1-103">Meghívhatja az IoT-központ feladatátvételi folyamatát a geopáros katasztrófa-helyreállítási régióra.</span><span class="sxs-lookup"><span data-stu-id="6a4e1-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="6a4e1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6a4e1-104">SYNTAX</span></span>

### <span data-ttu-id="6a4e1-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a4e1-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a4e1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6a4e1-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a4e1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6a4e1-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a4e1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6a4e1-108">DESCRIPTION</span></span>
<span data-ttu-id="6a4e1-109">Ez elindítja az IoT-központ feladatátvételét a másodlagos helyre.</span><span class="sxs-lookup"><span data-stu-id="6a4e1-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="6a4e1-110">Ez a művelet időt és telemetriai vesztést okoz a megoldásnak.</span><span class="sxs-lookup"><span data-stu-id="6a4e1-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="6a4e1-111">Ez egy hosszú futású művelet, amely néhány percig is eltarthat.</span><span class="sxs-lookup"><span data-stu-id="6a4e1-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="6a4e1-112">Kérjük, legyen körültekintő a használata során.</span><span class="sxs-lookup"><span data-stu-id="6a4e1-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="6a4e1-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6a4e1-113">EXAMPLES</span></span>

### <span data-ttu-id="6a4e1-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="6a4e1-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="6a4e1-115">A "myiothub" IoT-központ feladatátvételi folyamatának kezdeményezése.</span><span class="sxs-lookup"><span data-stu-id="6a4e1-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="6a4e1-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="6a4e1-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="6a4e1-117">A "myiothub" IoT-központ feladatátvételi folyamatának kezdeményezése a háttérben.</span><span class="sxs-lookup"><span data-stu-id="6a4e1-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="6a4e1-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a4e1-118">PARAMETERS</span></span>

### <span data-ttu-id="6a4e1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a4e1-119">-AsJob</span></span>
<span data-ttu-id="6a4e1-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6a4e1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a4e1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a4e1-121">-DefaultProfile</span></span>
<span data-ttu-id="6a4e1-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a4e1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a4e1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a4e1-123">-InputObject</span></span>
<span data-ttu-id="6a4e1-124">Iot Hub objektum</span><span class="sxs-lookup"><span data-stu-id="6a4e1-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="6a4e1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6a4e1-125">-Name</span></span>
<span data-ttu-id="6a4e1-126">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="6a4e1-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6a4e1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a4e1-127">-PassThru</span></span>
<span data-ttu-id="6a4e1-128">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="6a4e1-128">Allows to return the boolean object.</span></span> <span data-ttu-id="6a4e1-129">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6a4e1-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6a4e1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a4e1-130">-ResourceGroupName</span></span>
<span data-ttu-id="6a4e1-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6a4e1-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6a4e1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a4e1-132">-ResourceId</span></span>
<span data-ttu-id="6a4e1-133">Iot Hub Resource Id</span><span class="sxs-lookup"><span data-stu-id="6a4e1-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="6a4e1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a4e1-134">-Confirm</span></span>
<span data-ttu-id="6a4e1-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6a4e1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a4e1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a4e1-136">-WhatIf</span></span>
<span data-ttu-id="6a4e1-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6a4e1-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a4e1-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a4e1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a4e1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a4e1-139">CommonParameters</span></span>
<span data-ttu-id="6a4e1-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a4e1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a4e1-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a4e1-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a4e1-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a4e1-142">INPUTS</span></span>

### <span data-ttu-id="6a4e1-143">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6a4e1-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6a4e1-144">System.String</span><span class="sxs-lookup"><span data-stu-id="6a4e1-144">System.String</span></span>

## <span data-ttu-id="6a4e1-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a4e1-145">OUTPUTS</span></span>

### <span data-ttu-id="6a4e1-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6a4e1-146">System.Boolean</span></span>

## <span data-ttu-id="6a4e1-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6a4e1-147">NOTES</span></span>

## <span data-ttu-id="6a4e1-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a4e1-148">RELATED LINKS</span></span>
