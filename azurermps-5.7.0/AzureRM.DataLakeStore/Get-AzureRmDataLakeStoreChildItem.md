---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
ms.openlocfilehash: 6477a9f8c3830fa8ca8a74780db560455eb61dfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498976"
---
# <span data-ttu-id="664eb-101">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="664eb-101">Get-AzureRmDataLakeStoreChildItem</span></span>

## <span data-ttu-id="664eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="664eb-102">SYNOPSIS</span></span>
<span data-ttu-id="664eb-103">Az elemek listájának beolvasása az adattó áruházban lévő mappákban.</span><span class="sxs-lookup"><span data-stu-id="664eb-103">Gets the list of items in a folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="664eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="664eb-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="664eb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="664eb-105">DESCRIPTION</span></span>
<span data-ttu-id="664eb-106">A **Get-AzureRmDataLakeStoreChildItem** parancsmag az adattó-tárolóban lévő elemek listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="664eb-106">The **Get-AzureRmDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="664eb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="664eb-107">EXAMPLES</span></span>

### <span data-ttu-id="664eb-108">Példa 1: egy mappa alárendelt elemeinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="664eb-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="664eb-109">Ez a parancs beolvassa a MyFiles mappa alárendelt elemeit.</span><span class="sxs-lookup"><span data-stu-id="664eb-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="664eb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="664eb-110">PARAMETERS</span></span>

### <span data-ttu-id="664eb-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="664eb-111">-Account</span></span>
<span data-ttu-id="664eb-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="664eb-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="664eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="664eb-113">-DefaultProfile</span></span>
<span data-ttu-id="664eb-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="664eb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="664eb-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="664eb-115">-Path</span></span>
<span data-ttu-id="664eb-116">A mappa Data Lake Store elérési útját adja meg a gyökérkönyvtártól (/) kezdve.</span><span class="sxs-lookup"><span data-stu-id="664eb-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="664eb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="664eb-117">CommonParameters</span></span>
<span data-ttu-id="664eb-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="664eb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="664eb-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="664eb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="664eb-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="664eb-120">INPUTS</span></span>

### <span data-ttu-id="664eb-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="664eb-121">None</span></span>
<span data-ttu-id="664eb-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="664eb-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="664eb-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="664eb-123">OUTPUTS</span></span>

### <span data-ttu-id="664eb-124">IEnumerable<DataLakeStoreItem></span><span class="sxs-lookup"><span data-stu-id="664eb-124">IEnumerable<DataLakeStoreItem></span></span>
<span data-ttu-id="664eb-125">Az adattó fájljait és mappáit tároló lista a megadott elérési úton.</span><span class="sxs-lookup"><span data-stu-id="664eb-125">The list of Data Lake Store files and folders under the specified path.</span></span>

## <span data-ttu-id="664eb-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="664eb-126">NOTES</span></span>

## <span data-ttu-id="664eb-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="664eb-127">RELATED LINKS</span></span>

