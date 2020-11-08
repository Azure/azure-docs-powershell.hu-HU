---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184917"
---
# <span data-ttu-id="9f6d7-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="9f6d7-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="9f6d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6d7-103">IoT-hub lekérdezése hatékony SQL-szerű nyelv használatával.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="9f6d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f6d7-104">SYNTAX</span></span>

### <span data-ttu-id="9f6d7-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f6d7-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f6d7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9f6d7-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f6d7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9f6d7-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f6d7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f6d7-108">DESCRIPTION</span></span>
<span data-ttu-id="9f6d7-109">A IoT-hub lekérdezése erős SQL-szerű nyelv segítségével az eszközök és a modulokra, a munkahelyekre és az üzenetek továbbítására vonatkozó információk lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="9f6d7-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-languageTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="9f6d7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9f6d7-111">EXAMPLES</span></span>

### <span data-ttu-id="9f6d7-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9f6d7-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="9f6d7-113">Az összes eszköz különálló adatainak lekérdezése az Azure IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="9f6d7-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="9f6d7-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="9f6d7-115">Lekérdezés Top 2 modul Twin Data on a céleszköz.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="9f6d7-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f6d7-116">PARAMETERS</span></span>

### <span data-ttu-id="9f6d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f6d7-117">-DefaultProfile</span></span>
<span data-ttu-id="9f6d7-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f6d7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f6d7-119">-InputObject</span></span>
<span data-ttu-id="9f6d7-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="9f6d7-120">IotHub object</span></span>

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

### <span data-ttu-id="9f6d7-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9f6d7-121">-IotHubName</span></span>
<span data-ttu-id="9f6d7-122">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="9f6d7-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9f6d7-123">-Query</span><span class="sxs-lookup"><span data-stu-id="9f6d7-123">-Query</span></span>
<span data-ttu-id="9f6d7-124">Végrehajtani kívánt felhasználói lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-124">User query to be executed.</span></span>

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

### <span data-ttu-id="9f6d7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f6d7-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f6d7-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9f6d7-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9f6d7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f6d7-127">-ResourceId</span></span>
<span data-ttu-id="9f6d7-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="9f6d7-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9f6d7-129">-Top</span><span class="sxs-lookup"><span data-stu-id="9f6d7-129">-Top</span></span>
<span data-ttu-id="9f6d7-130">A visszaadni kívánt elemek maximális száma</span><span class="sxs-lookup"><span data-stu-id="9f6d7-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="9f6d7-131">Alapértelmezés szerint a lekérdezésnek nincs kupakja.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="9f6d7-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9f6d7-132">-Confirm</span></span>
<span data-ttu-id="9f6d7-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f6d7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f6d7-134">-WhatIf</span></span>
<span data-ttu-id="9f6d7-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f6d7-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f6d7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6d7-137">CommonParameters</span></span>
<span data-ttu-id="9f6d7-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f6d7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6d7-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f6d7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6d7-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f6d7-140">INPUTS</span></span>

### <span data-ttu-id="9f6d7-141">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9f6d7-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9f6d7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9f6d7-142">System.String</span></span>

## <span data-ttu-id="9f6d7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f6d7-143">OUTPUTS</span></span>

### <span data-ttu-id="9f6d7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9f6d7-144">System.String</span></span>

## <span data-ttu-id="9f6d7-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f6d7-145">NOTES</span></span>

## <span data-ttu-id="9f6d7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f6d7-146">RELATED LINKS</span></span>
