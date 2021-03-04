---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: f9372a246e16e719db60f52922a8a416f3de10c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928018"
---
# <span data-ttu-id="93ce3-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="93ce3-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="93ce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="93ce3-103">Meghívhatja az IoT-központ feladatátvételi folyamatát a geopáros katasztrófa-helyreállítási régióra.</span><span class="sxs-lookup"><span data-stu-id="93ce3-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="93ce3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="93ce3-104">SYNTAX</span></span>

### <span data-ttu-id="93ce3-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="93ce3-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93ce3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="93ce3-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93ce3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="93ce3-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93ce3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="93ce3-108">DESCRIPTION</span></span>
<span data-ttu-id="93ce3-109">Ez elindítja az IoT-központ feladatátvételét a másodlagos helyre.</span><span class="sxs-lookup"><span data-stu-id="93ce3-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="93ce3-110">Ez a művelet időt és telemetriai vesztést okoz a megoldásnak.</span><span class="sxs-lookup"><span data-stu-id="93ce3-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="93ce3-111">Ez egy hosszú futású művelet, amely néhány percig is eltarthat.</span><span class="sxs-lookup"><span data-stu-id="93ce3-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="93ce3-112">Kérjük, legyen körültekintő a használata során.</span><span class="sxs-lookup"><span data-stu-id="93ce3-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="93ce3-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="93ce3-113">EXAMPLES</span></span>

### <span data-ttu-id="93ce3-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="93ce3-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="93ce3-115">A "myiothub" IoT-központ feladatátvételi folyamatának kezdeményezése.</span><span class="sxs-lookup"><span data-stu-id="93ce3-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="93ce3-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="93ce3-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="93ce3-117">A "myiothub" IoT-központ feladatátvételi folyamatának kezdeményezése a háttérben.</span><span class="sxs-lookup"><span data-stu-id="93ce3-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="93ce3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93ce3-118">PARAMETERS</span></span>

### <span data-ttu-id="93ce3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93ce3-119">-AsJob</span></span>
<span data-ttu-id="93ce3-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="93ce3-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93ce3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ce3-121">-DefaultProfile</span></span>
<span data-ttu-id="93ce3-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93ce3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93ce3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93ce3-123">-InputObject</span></span>
<span data-ttu-id="93ce3-124">Iot Hub objektum</span><span class="sxs-lookup"><span data-stu-id="93ce3-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="93ce3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="93ce3-125">-Name</span></span>
<span data-ttu-id="93ce3-126">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="93ce3-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="93ce3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93ce3-127">-PassThru</span></span>
<span data-ttu-id="93ce3-128">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="93ce3-128">Allows to return the boolean object.</span></span> <span data-ttu-id="93ce3-129">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="93ce3-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="93ce3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93ce3-130">-ResourceGroupName</span></span>
<span data-ttu-id="93ce3-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="93ce3-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="93ce3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93ce3-132">-ResourceId</span></span>
<span data-ttu-id="93ce3-133">Iot Hub Resource Id</span><span class="sxs-lookup"><span data-stu-id="93ce3-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="93ce3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93ce3-134">-Confirm</span></span>
<span data-ttu-id="93ce3-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="93ce3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93ce3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93ce3-136">-WhatIf</span></span>
<span data-ttu-id="93ce3-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="93ce3-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93ce3-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93ce3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93ce3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ce3-139">CommonParameters</span></span>
<span data-ttu-id="93ce3-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93ce3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ce3-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ce3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ce3-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93ce3-142">INPUTS</span></span>

### <span data-ttu-id="93ce3-143">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="93ce3-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="93ce3-144">System.String</span><span class="sxs-lookup"><span data-stu-id="93ce3-144">System.String</span></span>

## <span data-ttu-id="93ce3-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93ce3-145">OUTPUTS</span></span>

### <span data-ttu-id="93ce3-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93ce3-146">System.Boolean</span></span>

## <span data-ttu-id="93ce3-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="93ce3-147">NOTES</span></span>

## <span data-ttu-id="93ce3-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93ce3-148">RELATED LINKS</span></span>
