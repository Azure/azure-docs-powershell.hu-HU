---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154867"
---
# <span data-ttu-id="3bedf-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="3bedf-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="3bedf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bedf-102">SYNOPSIS</span></span>
<span data-ttu-id="3bedf-103">Egy hatékony, SQL-hez hasonló nyelvet használva lekérdezheti az IoT-központot.</span><span class="sxs-lookup"><span data-stu-id="3bedf-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="3bedf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3bedf-104">SYNTAX</span></span>

### <span data-ttu-id="3bedf-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3bedf-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bedf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3bedf-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bedf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3bedf-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bedf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3bedf-108">DESCRIPTION</span></span>
<span data-ttu-id="3bedf-109">Az IoT-központban egy hatékony SQL-hez hasonló nyelven lekérdezheti az eszköz- és modullekérdezésekkel, a feladatokkal és az üzenetek átirányításával kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="3bedf-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="3bedf-110">További https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="3bedf-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="3bedf-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3bedf-111">EXAMPLES</span></span>

### <span data-ttu-id="3bedf-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="3bedf-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="3bedf-113">Lekérdezheti az összes eszköz eszközét egy Azure IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="3bedf-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="3bedf-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="3bedf-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="3bedf-115">Lekérdezés a 2 modul legfelső adatokat egy céleszközön.</span><span class="sxs-lookup"><span data-stu-id="3bedf-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="3bedf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bedf-116">PARAMETERS</span></span>

### <span data-ttu-id="3bedf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bedf-117">-DefaultProfile</span></span>
<span data-ttu-id="3bedf-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bedf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bedf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bedf-119">-InputObject</span></span>
<span data-ttu-id="3bedf-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="3bedf-120">IotHub object</span></span>

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

### <span data-ttu-id="3bedf-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3bedf-121">-IotHubName</span></span>
<span data-ttu-id="3bedf-122">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="3bedf-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3bedf-123">-Query</span><span class="sxs-lookup"><span data-stu-id="3bedf-123">-Query</span></span>
<span data-ttu-id="3bedf-124">Végrehajtandó felhasználói lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="3bedf-124">User query to be executed.</span></span>

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

### <span data-ttu-id="3bedf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bedf-125">-ResourceGroupName</span></span>
<span data-ttu-id="3bedf-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3bedf-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3bedf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bedf-127">-ResourceId</span></span>
<span data-ttu-id="3bedf-128">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3bedf-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3bedf-129">-Top</span><span class="sxs-lookup"><span data-stu-id="3bedf-129">-Top</span></span>
<span data-ttu-id="3bedf-130">A vissza nem térhet elemek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="3bedf-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="3bedf-131">Alapértelmezés szerint a lekérdezésben nincs nagybetű.</span><span class="sxs-lookup"><span data-stu-id="3bedf-131">By default query has no cap.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bedf-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bedf-132">-Confirm</span></span>
<span data-ttu-id="3bedf-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3bedf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bedf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bedf-134">-WhatIf</span></span>
<span data-ttu-id="3bedf-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3bedf-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bedf-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3bedf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bedf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bedf-137">CommonParameters</span></span>
<span data-ttu-id="3bedf-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bedf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bedf-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bedf-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bedf-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3bedf-140">INPUTS</span></span>

### <span data-ttu-id="3bedf-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3bedf-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3bedf-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3bedf-142">System.String</span></span>

## <span data-ttu-id="3bedf-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bedf-143">OUTPUTS</span></span>

### <span data-ttu-id="3bedf-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3bedf-144">System.String</span></span>

## <span data-ttu-id="3bedf-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3bedf-145">NOTES</span></span>

## <span data-ttu-id="3bedf-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bedf-146">RELATED LINKS</span></span>
