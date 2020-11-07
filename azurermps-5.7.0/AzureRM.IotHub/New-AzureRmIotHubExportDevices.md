---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubexportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 2f9122b2683721aa7f92bc1695b6c314e83d76c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680161"
---
# <span data-ttu-id="daf7a-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="daf7a-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="daf7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="daf7a-102">SYNOPSIS</span></span>
<span data-ttu-id="daf7a-103">Új exportálási eszközök feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="daf7a-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="daf7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="daf7a-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="daf7a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="daf7a-105">DESCRIPTION</span></span>
<span data-ttu-id="daf7a-106">Új exportálási eszközök feladatot hoz létre a IotHub.</span><span class="sxs-lookup"><span data-stu-id="daf7a-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="daf7a-107">Ezzel az összes eszközt exportálja a megadott tárolóba.</span><span class="sxs-lookup"><span data-stu-id="daf7a-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="daf7a-108">Az alábbi cikk bemutatja, hogy miként létrehozhatja a SAS-URI azonosítót.</span><span class="sxs-lookup"><span data-stu-id="daf7a-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="daf7a-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="daf7a-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="daf7a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="daf7a-110">EXAMPLES</span></span>

### <span data-ttu-id="daf7a-111">1. példa: az exportálási eszköz kérésének kibocsátása</span><span class="sxs-lookup"><span data-stu-id="daf7a-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys $true
```

<span data-ttu-id="daf7a-112">Új exportfájl-kérést hoz létre a "myiothub" IotHub, kivéve a billentyűket.</span><span class="sxs-lookup"><span data-stu-id="daf7a-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="daf7a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="daf7a-113">PARAMETERS</span></span>

### <span data-ttu-id="daf7a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf7a-114">-DefaultProfile</span></span>
<span data-ttu-id="daf7a-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="daf7a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf7a-116">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="daf7a-116">-ExportBlobContainerUri</span></span>
<span data-ttu-id="daf7a-117">Az URI, amelybe a blobot exportálni kívánja.</span><span class="sxs-lookup"><span data-stu-id="daf7a-117">The Uri to export the blob to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf7a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="daf7a-118">-Name</span></span>
<span data-ttu-id="daf7a-119">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="daf7a-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daf7a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daf7a-120">-ResourceGroupName</span></span>
<span data-ttu-id="daf7a-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="daf7a-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daf7a-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="daf7a-122">-Confirm</span></span>
<span data-ttu-id="daf7a-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="daf7a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf7a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daf7a-124">-WhatIf</span></span>
<span data-ttu-id="daf7a-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="daf7a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daf7a-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="daf7a-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf7a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf7a-127">CommonParameters</span></span>
<span data-ttu-id="daf7a-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="daf7a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf7a-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daf7a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf7a-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="daf7a-130">INPUTS</span></span>

### <span data-ttu-id="daf7a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="daf7a-131">System.String</span></span>

## <span data-ttu-id="daf7a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="daf7a-132">OUTPUTS</span></span>

### <span data-ttu-id="daf7a-133">Microsoft. Azure. Management. IotHub. models. JobResponse</span><span class="sxs-lookup"><span data-stu-id="daf7a-133">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="daf7a-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="daf7a-134">NOTES</span></span>

## <span data-ttu-id="daf7a-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="daf7a-135">RELATED LINKS</span></span>

