---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: b1a570d2821606944d4afde21919dad8832ed380
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672266"
---
# <span data-ttu-id="c7edc-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7edc-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="c7edc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7edc-102">SYNOPSIS</span></span>
<span data-ttu-id="c7edc-103">Az adattó áruházban lévő fájlok vagy mappák részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c7edc-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7edc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7edc-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7edc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7edc-105">DESCRIPTION</span></span>
<span data-ttu-id="c7edc-106">A **Get-AzureRmDataLakeStoreItem** parancsmag az adatok tava áruházban található fájlok vagy mappák részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c7edc-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c7edc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c7edc-107">EXAMPLES</span></span>

### <span data-ttu-id="c7edc-108">1. példa: az adattó áruházból származó fájlok adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="c7edc-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="c7edc-109">Ez a parancs az adattó áruházból Test.csv fájl részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c7edc-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="c7edc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7edc-110">PARAMETERS</span></span>

### <span data-ttu-id="c7edc-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="c7edc-111">-Account</span></span>
<span data-ttu-id="c7edc-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7edc-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c7edc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7edc-113">-DefaultProfile</span></span>
<span data-ttu-id="c7edc-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7edc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7edc-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="c7edc-115">-Path</span></span>
<span data-ttu-id="c7edc-116">Az adattó-tároló elérési útját adja meg, amelyből egy elem részleteit kapja meg, kezdve a legfelső szintű könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="c7edc-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7edc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7edc-117">CommonParameters</span></span>
<span data-ttu-id="c7edc-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7edc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7edc-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7edc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7edc-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7edc-120">INPUTS</span></span>

### <span data-ttu-id="c7edc-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="c7edc-121">None</span></span>
<span data-ttu-id="c7edc-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c7edc-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7edc-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7edc-123">OUTPUTS</span></span>

### <span data-ttu-id="c7edc-124">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7edc-124">DataLakeStoreItem</span></span>
<span data-ttu-id="c7edc-125">A megadott elérési úton lévő fájl vagy mappa</span><span class="sxs-lookup"><span data-stu-id="c7edc-125">The file or folder at the path specified.</span></span>

## <span data-ttu-id="c7edc-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7edc-126">NOTES</span></span>

## <span data-ttu-id="c7edc-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7edc-127">RELATED LINKS</span></span>

[<span data-ttu-id="c7edc-128">Exportálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7edc-128">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c7edc-129">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="c7edc-129">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="c7edc-130">Importálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7edc-130">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c7edc-131">Bekapcsolódás a AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7edc-131">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c7edc-132">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7edc-132">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c7edc-133">Új – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7edc-133">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c7edc-134">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7edc-134">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c7edc-135">Teszt-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7edc-135">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


