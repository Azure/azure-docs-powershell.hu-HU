---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubexportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 4c13a6366f0ccae803e8020f16bf2b566bd70934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497439"
---
# <span data-ttu-id="a8219-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="a8219-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="a8219-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8219-102">SYNOPSIS</span></span>
<span data-ttu-id="a8219-103">Új exportálási eszközök feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a8219-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8219-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8219-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8219-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8219-105">DESCRIPTION</span></span>
<span data-ttu-id="a8219-106">Új exportálási eszközök feladatot hoz létre a IotHub.</span><span class="sxs-lookup"><span data-stu-id="a8219-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="a8219-107">Ezzel az összes eszközt exportálja a megadott tárolóba.</span><span class="sxs-lookup"><span data-stu-id="a8219-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="a8219-108">Az alábbi cikk bemutatja, hogy miként létrehozhatja a SAS-URI azonosítót.</span><span class="sxs-lookup"><span data-stu-id="a8219-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="a8219-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="a8219-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="a8219-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a8219-110">EXAMPLES</span></span>

### <span data-ttu-id="a8219-111">1. példa: az exportálási eszköz kérésének kibocsátása</span><span class="sxs-lookup"><span data-stu-id="a8219-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="a8219-112">Új exportfájl-kérést hoz létre a "myiothub" IotHub, kivéve a billentyűket.</span><span class="sxs-lookup"><span data-stu-id="a8219-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="a8219-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8219-113">PARAMETERS</span></span>

### <span data-ttu-id="a8219-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8219-114">-DefaultProfile</span></span>
<span data-ttu-id="a8219-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a8219-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8219-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="a8219-116">-ExcludeKeys</span></span>
<span data-ttu-id="a8219-117">Lehetővé teszi a kulcsok nélküli eszközök exportálását.</span><span class="sxs-lookup"><span data-stu-id="a8219-117">Allows to export devices without keys.</span></span>

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

### <span data-ttu-id="a8219-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="a8219-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="a8219-119">Az URI, amelybe a blobot exportálni kívánja.</span><span class="sxs-lookup"><span data-stu-id="a8219-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="a8219-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8219-120">-Name</span></span>
<span data-ttu-id="a8219-121">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="a8219-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="a8219-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8219-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8219-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a8219-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a8219-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a8219-124">-Confirm</span></span>
<span data-ttu-id="a8219-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8219-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8219-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8219-126">-WhatIf</span></span>
<span data-ttu-id="a8219-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a8219-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8219-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8219-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8219-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8219-129">CommonParameters</span></span>
<span data-ttu-id="a8219-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8219-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8219-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8219-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8219-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8219-132">INPUTS</span></span>

### <span data-ttu-id="a8219-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a8219-133">System.String</span></span>

## <span data-ttu-id="a8219-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8219-134">OUTPUTS</span></span>

### <span data-ttu-id="a8219-135">Microsoft. Azure. Command. Management. IotHub. models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="a8219-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="a8219-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8219-136">NOTES</span></span>

## <span data-ttu-id="a8219-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8219-137">RELATED LINKS</span></span>
