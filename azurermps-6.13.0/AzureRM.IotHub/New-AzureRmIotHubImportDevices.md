---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubimportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
ms.openlocfilehash: 37445e2f88172c3a9e703c85562518212baa9e83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497435"
---
# <span data-ttu-id="d2449-101">New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="d2449-101">New-AzureRmIotHubImportDevices</span></span>

## <span data-ttu-id="d2449-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2449-102">SYNOPSIS</span></span>
<span data-ttu-id="d2449-103">Új importálási eszközök feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d2449-103">Creates a new import devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2449-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2449-104">SYNTAX</span></span>

```
New-AzureRmIotHubImportDevices [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2449-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2449-105">DESCRIPTION</span></span>
<span data-ttu-id="d2449-106">Új importálási eszközök feladatot hoz létre a IotHub.</span><span class="sxs-lookup"><span data-stu-id="d2449-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="d2449-107">Ezzel a megadott tárolóból importálja az összes eszközt a IotHub.</span><span class="sxs-lookup"><span data-stu-id="d2449-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="d2449-108">Az alábbi cikk bemutatja, hogy miként létrehozhatja a SAS-URI azonosítót.</span><span class="sxs-lookup"><span data-stu-id="d2449-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="d2449-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="d2449-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="d2449-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d2449-110">EXAMPLES</span></span>

### <span data-ttu-id="d2449-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d2449-111">Example 1</span></span>
```
PS C:\> New-AzureRmIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="d2449-112">Új importálási eszközre vonatkozó kérelmet hoz létre a "myiothub" IotHub.</span><span class="sxs-lookup"><span data-stu-id="d2449-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="d2449-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2449-113">PARAMETERS</span></span>

### <span data-ttu-id="d2449-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2449-114">-DefaultProfile</span></span>
<span data-ttu-id="d2449-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d2449-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2449-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="d2449-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="d2449-117">Beviteli blob tároló URI a FileUpload-hoz</span><span class="sxs-lookup"><span data-stu-id="d2449-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="d2449-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d2449-118">-Name</span></span>
<span data-ttu-id="d2449-119">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="d2449-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="d2449-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="d2449-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="d2449-121">Az URI a kimenet írásához.</span><span class="sxs-lookup"><span data-stu-id="d2449-121">The Uri to write the output to.</span></span> 

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

### <span data-ttu-id="d2449-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2449-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2449-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d2449-123">Resource Group Name</span></span>

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

### <span data-ttu-id="d2449-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d2449-124">-Confirm</span></span>
<span data-ttu-id="d2449-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d2449-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2449-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2449-126">-WhatIf</span></span>
<span data-ttu-id="d2449-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d2449-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2449-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d2449-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2449-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2449-129">CommonParameters</span></span>
<span data-ttu-id="d2449-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2449-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2449-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2449-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2449-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2449-132">INPUTS</span></span>

### <span data-ttu-id="d2449-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d2449-133">System.String</span></span>

## <span data-ttu-id="d2449-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2449-134">OUTPUTS</span></span>

### <span data-ttu-id="d2449-135">Microsoft. Azure. Command. Management. IotHub. models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="d2449-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="d2449-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2449-136">NOTES</span></span>

## <span data-ttu-id="d2449-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2449-137">RELATED LINKS</span></span>
