---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 3191f4e451ec010a3918130142d08da6f08b3990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504136"
---
# <span data-ttu-id="10fd2-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="10fd2-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="10fd2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="10fd2-103">Új exportálási eszközök feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="10fd2-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10fd2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10fd2-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10fd2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="10fd2-105">DESCRIPTION</span></span>
<span data-ttu-id="10fd2-106">Új exportálási eszközök feladatot hoz létre a IotHub.</span><span class="sxs-lookup"><span data-stu-id="10fd2-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="10fd2-107">Ezzel az összes eszközt exportálja a megadott tárolóba.</span><span class="sxs-lookup"><span data-stu-id="10fd2-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="10fd2-108">Az alábbi cikk bemutatja, hogy miként létrehozhatja a SAS-URI azonosítót.</span><span class="sxs-lookup"><span data-stu-id="10fd2-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="10fd2-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="10fd2-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="10fd2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="10fd2-110">EXAMPLES</span></span>

### <span data-ttu-id="10fd2-111">1. példa: az exportálási eszköz kérésének kibocsátása</span><span class="sxs-lookup"><span data-stu-id="10fd2-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys $true
```

<span data-ttu-id="10fd2-112">Új exportfájl-kérést hoz létre a "myiothub" IotHub, kivéve a billentyűket.</span><span class="sxs-lookup"><span data-stu-id="10fd2-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="10fd2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10fd2-113">PARAMETERS</span></span>

### <span data-ttu-id="10fd2-114">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="10fd2-114">-ExportBlobContainerUri</span></span>
<span data-ttu-id="10fd2-115">Az URI, amelybe a blobot exportálni kívánja.</span><span class="sxs-lookup"><span data-stu-id="10fd2-115">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="10fd2-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="10fd2-116">-Name</span></span>
<span data-ttu-id="10fd2-117">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="10fd2-117">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10fd2-118">-ResourceGroupName</span></span>
<span data-ttu-id="10fd2-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="10fd2-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd2-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="10fd2-120">-Confirm</span></span>
<span data-ttu-id="10fd2-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="10fd2-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10fd2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10fd2-122">-WhatIf</span></span>
<span data-ttu-id="10fd2-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="10fd2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10fd2-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="10fd2-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10fd2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10fd2-125">-DefaultProfile</span></span>
<span data-ttu-id="10fd2-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10fd2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10fd2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10fd2-127">CommonParameters</span></span>
<span data-ttu-id="10fd2-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10fd2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10fd2-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10fd2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10fd2-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10fd2-130">INPUTS</span></span>

### <span data-ttu-id="10fd2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="10fd2-131">System.String</span></span>

## <span data-ttu-id="10fd2-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10fd2-132">OUTPUTS</span></span>

### <span data-ttu-id="10fd2-133">Microsoft. Azure. Management. IotHub. models. JobResponse</span><span class="sxs-lookup"><span data-stu-id="10fd2-133">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="10fd2-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10fd2-134">NOTES</span></span>

## <span data-ttu-id="10fd2-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10fd2-135">RELATED LINKS</span></span>

