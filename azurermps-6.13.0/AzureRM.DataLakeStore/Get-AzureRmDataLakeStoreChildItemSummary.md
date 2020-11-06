---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azureatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItemSummary.md
ms.openlocfilehash: 83fb8b3ea5fdf9ad63983d2a3a3d23d402fbb5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502960"
---
# <span data-ttu-id="8f0ee-101">Get-AzureRmDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="8f0ee-101">Get-AzureRmDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="8f0ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f0ee-102">SYNOPSIS</span></span>
<span data-ttu-id="8f0ee-103">A megadott elérési úton lévő teljes méret, fájlok és könyvtárak összegzése</span><span class="sxs-lookup"><span data-stu-id="8f0ee-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f0ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f0ee-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f0ee-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f0ee-105">DESCRIPTION</span></span>
<span data-ttu-id="8f0ee-106">A **Get-AzureRmDataLakeStoreChildItemSummary** lekéri egy adott útvonal tartalmi összegzését.</span><span class="sxs-lookup"><span data-stu-id="8f0ee-106">The **Get-AzureRmDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="8f0ee-107">A fájl, a könyvtárak és a megadott elérési út alatti fájlok teljes méretének kiszámítása.</span><span class="sxs-lookup"><span data-stu-id="8f0ee-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="8f0ee-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8f0ee-108">EXAMPLES</span></span>

### <span data-ttu-id="8f0ee-109">Példa 1: mappa tartalmi összegzésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="8f0ee-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="8f0ee-110">Felsorolja a teljes könyvtárak számát, a fájlok és a/a. alatti méretet.</span><span class="sxs-lookup"><span data-stu-id="8f0ee-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="8f0ee-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f0ee-111">PARAMETERS</span></span>

### <span data-ttu-id="8f0ee-112">-Fiók</span><span class="sxs-lookup"><span data-stu-id="8f0ee-112">-Account</span></span>
<span data-ttu-id="8f0ee-113">Az adattó áruházbeli fiókja a FileSystem művelet végrehajtásához</span><span class="sxs-lookup"><span data-stu-id="8f0ee-113">The Data Lake Store account to execute the filesystem operation in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f0ee-114">-Párhuzamosság</span><span class="sxs-lookup"><span data-stu-id="8f0ee-114">-Concurrency</span></span>
<span data-ttu-id="8f0ee-115">A párhuzamosan feldolgozott fájlok/könyvtárak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="8f0ee-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="8f0ee-116">Az alapértelmezett beállítás a rendszerspecifikáción alapuló legjobb munkamennyiségként fog kiszámításra.</span><span class="sxs-lookup"><span data-stu-id="8f0ee-116">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f0ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f0ee-117">-DefaultProfile</span></span>
<span data-ttu-id="8f0ee-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f0ee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f0ee-119">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="8f0ee-119">-Path</span></span>
<span data-ttu-id="8f0ee-120">A megadott adattó-fiók útvonala, amelyet le kell olvasnia.</span><span class="sxs-lookup"><span data-stu-id="8f0ee-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="8f0ee-121">A "/Folder/file.txt" formátumban lehet fájl vagy mappa, ahol az első "/" a DNS a fájlrendszer gyökerét jelzi.</span><span class="sxs-lookup"><span data-stu-id="8f0ee-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f0ee-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8f0ee-122">-Confirm</span></span>
<span data-ttu-id="8f0ee-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f0ee-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f0ee-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f0ee-124">-WhatIf</span></span>
<span data-ttu-id="8f0ee-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8f0ee-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f0ee-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f0ee-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f0ee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f0ee-127">CommonParameters</span></span>
<span data-ttu-id="8f0ee-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f0ee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f0ee-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f0ee-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f0ee-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f0ee-130">INPUTS</span></span>

### <span data-ttu-id="8f0ee-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8f0ee-131">System.String</span></span>

### <span data-ttu-id="8f0ee-132">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="8f0ee-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="8f0ee-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8f0ee-133">System.Int32</span></span>

## <span data-ttu-id="8f0ee-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f0ee-134">OUTPUTS</span></span>

### <span data-ttu-id="8f0ee-135">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="8f0ee-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="8f0ee-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f0ee-136">NOTES</span></span>

## <span data-ttu-id="8f0ee-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f0ee-137">RELATED LINKS</span></span>
