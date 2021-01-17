---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350946"
---
# <span data-ttu-id="358d5-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="358d5-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="358d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="358d5-102">SYNOPSIS</span></span>
<span data-ttu-id="358d5-103">Meghívhatja az IoT-központ feladatátvételi folyamatát a geopáros katasztrófa-helyreállítási régióra.</span><span class="sxs-lookup"><span data-stu-id="358d5-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="358d5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="358d5-104">SYNTAX</span></span>

### <span data-ttu-id="358d5-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="358d5-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="358d5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="358d5-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="358d5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="358d5-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="358d5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="358d5-108">DESCRIPTION</span></span>
<span data-ttu-id="358d5-109">Ez elindítja az IoT-központ feladatátvételét a másodlagos helyre.</span><span class="sxs-lookup"><span data-stu-id="358d5-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="358d5-110">Ez a művelet időt és telemetriai vesztést okoz a megoldásnak.</span><span class="sxs-lookup"><span data-stu-id="358d5-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="358d5-111">Ez egy hosszú futású művelet, amely néhány percig is eltarthat.</span><span class="sxs-lookup"><span data-stu-id="358d5-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="358d5-112">Kérjük, legyen körültekintő a használata során.</span><span class="sxs-lookup"><span data-stu-id="358d5-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="358d5-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="358d5-113">EXAMPLES</span></span>

### <span data-ttu-id="358d5-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="358d5-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="358d5-115">A "myiothub" IoT-központ feladatátvételi folyamatának kezdeményezése.</span><span class="sxs-lookup"><span data-stu-id="358d5-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="358d5-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="358d5-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="358d5-117">A "myiothub" IoT-központ feladatátvételi folyamatának kezdeményezése a háttérben.</span><span class="sxs-lookup"><span data-stu-id="358d5-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="358d5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="358d5-118">PARAMETERS</span></span>

### <span data-ttu-id="358d5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="358d5-119">-AsJob</span></span>
<span data-ttu-id="358d5-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="358d5-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="358d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="358d5-121">-DefaultProfile</span></span>
<span data-ttu-id="358d5-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="358d5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="358d5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="358d5-123">-InputObject</span></span>
<span data-ttu-id="358d5-124">Iot Hub objektum</span><span class="sxs-lookup"><span data-stu-id="358d5-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="358d5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="358d5-125">-Name</span></span>
<span data-ttu-id="358d5-126">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="358d5-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="358d5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="358d5-127">-PassThru</span></span>
<span data-ttu-id="358d5-128">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="358d5-128">Allows to return the boolean object.</span></span> <span data-ttu-id="358d5-129">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="358d5-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="358d5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="358d5-130">-ResourceGroupName</span></span>
<span data-ttu-id="358d5-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="358d5-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="358d5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="358d5-132">-ResourceId</span></span>
<span data-ttu-id="358d5-133">Iot Hub Resource Id</span><span class="sxs-lookup"><span data-stu-id="358d5-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="358d5-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="358d5-134">-Confirm</span></span>
<span data-ttu-id="358d5-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="358d5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="358d5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="358d5-136">-WhatIf</span></span>
<span data-ttu-id="358d5-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="358d5-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="358d5-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="358d5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="358d5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="358d5-139">CommonParameters</span></span>
<span data-ttu-id="358d5-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="358d5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="358d5-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="358d5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="358d5-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="358d5-142">INPUTS</span></span>

### <span data-ttu-id="358d5-143">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="358d5-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="358d5-144">System.String</span><span class="sxs-lookup"><span data-stu-id="358d5-144">System.String</span></span>

## <span data-ttu-id="358d5-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="358d5-145">OUTPUTS</span></span>

### <span data-ttu-id="358d5-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="358d5-146">System.Boolean</span></span>

## <span data-ttu-id="358d5-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="358d5-147">NOTES</span></span>

## <span data-ttu-id="358d5-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="358d5-148">RELATED LINKS</span></span>
