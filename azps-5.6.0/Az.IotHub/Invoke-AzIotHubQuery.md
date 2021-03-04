---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 955e09ab17644009f281223581ae2f5f45adfb33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918937"
---
# <span data-ttu-id="8f213-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="8f213-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="8f213-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f213-102">SYNOPSIS</span></span>
<span data-ttu-id="8f213-103">Egy hatékony, SQL-hez hasonló nyelvet használva lekérdezheti az IoT-központot.</span><span class="sxs-lookup"><span data-stu-id="8f213-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="8f213-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8f213-104">SYNTAX</span></span>

### <span data-ttu-id="8f213-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8f213-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f213-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8f213-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f213-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8f213-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f213-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8f213-108">DESCRIPTION</span></span>
<span data-ttu-id="8f213-109">Az IoT-központban egy hatékony SQL-hez hasonló nyelven lekérdezheti az eszköz- és modullekérdezésekkel, a feladatokkal és az üzenetek átirányításával kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="8f213-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="8f213-110">További https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="8f213-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="8f213-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8f213-111">EXAMPLES</span></span>

### <span data-ttu-id="8f213-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="8f213-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="8f213-113">Lekérdezheti az összes eszköz eszközét egy Azure IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="8f213-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="8f213-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="8f213-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="8f213-115">Lekérdezés a 2 modul legfelső adatokat egy céleszközön.</span><span class="sxs-lookup"><span data-stu-id="8f213-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="8f213-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f213-116">PARAMETERS</span></span>

### <span data-ttu-id="8f213-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f213-117">-DefaultProfile</span></span>
<span data-ttu-id="8f213-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f213-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f213-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f213-119">-InputObject</span></span>
<span data-ttu-id="8f213-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="8f213-120">IotHub object</span></span>

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

### <span data-ttu-id="8f213-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8f213-121">-IotHubName</span></span>
<span data-ttu-id="8f213-122">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="8f213-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8f213-123">-Query</span><span class="sxs-lookup"><span data-stu-id="8f213-123">-Query</span></span>
<span data-ttu-id="8f213-124">Végrehajtandó felhasználói lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="8f213-124">User query to be executed.</span></span>

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

### <span data-ttu-id="8f213-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f213-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f213-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8f213-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8f213-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f213-127">-ResourceId</span></span>
<span data-ttu-id="8f213-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="8f213-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8f213-129">-Top</span><span class="sxs-lookup"><span data-stu-id="8f213-129">-Top</span></span>
<span data-ttu-id="8f213-130">A vissza nem térhet elemek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="8f213-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="8f213-131">Alapértelmezés szerint a lekérdezésben nincs nagybetű.</span><span class="sxs-lookup"><span data-stu-id="8f213-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="8f213-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f213-132">-Confirm</span></span>
<span data-ttu-id="8f213-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8f213-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f213-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f213-134">-WhatIf</span></span>
<span data-ttu-id="8f213-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8f213-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f213-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f213-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f213-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f213-137">CommonParameters</span></span>
<span data-ttu-id="8f213-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f213-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f213-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f213-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f213-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f213-140">INPUTS</span></span>

### <span data-ttu-id="8f213-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8f213-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8f213-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8f213-142">System.String</span></span>

## <span data-ttu-id="8f213-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f213-143">OUTPUTS</span></span>

### <span data-ttu-id="8f213-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8f213-144">System.String</span></span>

## <span data-ttu-id="8f213-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8f213-145">NOTES</span></span>

## <span data-ttu-id="8f213-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f213-146">RELATED LINKS</span></span>
