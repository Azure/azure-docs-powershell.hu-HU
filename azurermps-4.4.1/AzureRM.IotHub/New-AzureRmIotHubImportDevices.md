---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
ms.openlocfilehash: f8c2d2b7508e07dd5f42287a95623c3a6cf245de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504132"
---
# <span data-ttu-id="562fd-101">New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="562fd-101">New-AzureRmIotHubImportDevices</span></span>

## <span data-ttu-id="562fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="562fd-102">SYNOPSIS</span></span>
<span data-ttu-id="562fd-103">Új importálási eszközök feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="562fd-103">Creates a new import devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="562fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="562fd-104">SYNTAX</span></span>

```
New-AzureRmIotHubImportDevices [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="562fd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="562fd-105">DESCRIPTION</span></span>
<span data-ttu-id="562fd-106">Új importálási eszközök feladatot hoz létre a IotHub.</span><span class="sxs-lookup"><span data-stu-id="562fd-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="562fd-107">Ezzel a megadott tárolóból importálja az összes eszközt a IotHub.</span><span class="sxs-lookup"><span data-stu-id="562fd-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="562fd-108">Az alábbi cikk bemutatja, hogy miként létrehozhatja a SAS-URI azonosítót.</span><span class="sxs-lookup"><span data-stu-id="562fd-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="562fd-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="562fd-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="562fd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="562fd-110">EXAMPLES</span></span>

### <span data-ttu-id="562fd-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="562fd-111">Example 1</span></span>
```
PS C:\> New-AzureRmIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="562fd-112">Új importálási eszközre vonatkozó kérelmet hoz létre a "myiothub" IotHub.</span><span class="sxs-lookup"><span data-stu-id="562fd-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="562fd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="562fd-113">PARAMETERS</span></span>

### <span data-ttu-id="562fd-114">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="562fd-114">-InputBlobContainerUri</span></span>
<span data-ttu-id="562fd-115">Beviteli blob tároló URI a FileUpload-hoz</span><span class="sxs-lookup"><span data-stu-id="562fd-115">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="562fd-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="562fd-116">-Name</span></span>
<span data-ttu-id="562fd-117">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="562fd-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="562fd-118">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="562fd-118">-OutputBlobContainerUri</span></span>
<span data-ttu-id="562fd-119">Az URI a kimenet írásához.</span><span class="sxs-lookup"><span data-stu-id="562fd-119">The Uri to write the output to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="562fd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="562fd-120">-ResourceGroupName</span></span>
<span data-ttu-id="562fd-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="562fd-121">Resource Group Name</span></span>

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

### <span data-ttu-id="562fd-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="562fd-122">-Confirm</span></span>
<span data-ttu-id="562fd-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="562fd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="562fd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="562fd-124">-WhatIf</span></span>
<span data-ttu-id="562fd-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="562fd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="562fd-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="562fd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="562fd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="562fd-127">-DefaultProfile</span></span>
<span data-ttu-id="562fd-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="562fd-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="562fd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="562fd-129">CommonParameters</span></span>
<span data-ttu-id="562fd-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="562fd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="562fd-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="562fd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="562fd-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="562fd-132">INPUTS</span></span>

### <span data-ttu-id="562fd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="562fd-133">System.String</span></span>

## <span data-ttu-id="562fd-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="562fd-134">OUTPUTS</span></span>

### <span data-ttu-id="562fd-135">Microsoft. Azure. Management. IotHub. models. JobResponse</span><span class="sxs-lookup"><span data-stu-id="562fd-135">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="562fd-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="562fd-136">NOTES</span></span>

## <span data-ttu-id="562fd-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="562fd-137">RELATED LINKS</span></span>

