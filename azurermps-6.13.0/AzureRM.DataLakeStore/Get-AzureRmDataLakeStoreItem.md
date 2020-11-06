---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a1e70286364fea53062a75b7ac886834803c3674
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502963"
---
# <span data-ttu-id="2ae31-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ae31-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="2ae31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ae31-102">SYNOPSIS</span></span>
<span data-ttu-id="2ae31-103">Az adattó áruházban lévő fájlok vagy mappák részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2ae31-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ae31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ae31-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ae31-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ae31-105">DESCRIPTION</span></span>
<span data-ttu-id="2ae31-106">A **Get-AzureRmDataLakeStoreItem** parancsmag az adatok tava áruházban található fájlok vagy mappák részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2ae31-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2ae31-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2ae31-107">EXAMPLES</span></span>

### <span data-ttu-id="2ae31-108">1. példa: az adattó áruházból származó fájlok adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="2ae31-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="2ae31-109">Ez a parancs az adattó áruházból Test.csv fájl részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2ae31-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="2ae31-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ae31-110">PARAMETERS</span></span>

### <span data-ttu-id="2ae31-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="2ae31-111">-Account</span></span>
<span data-ttu-id="2ae31-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ae31-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2ae31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ae31-113">-DefaultProfile</span></span>
<span data-ttu-id="2ae31-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ae31-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ae31-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="2ae31-115">-Path</span></span>
<span data-ttu-id="2ae31-116">Az adattó-tároló elérési útját adja meg, amelyből egy elem részleteit kapja meg, kezdve a legfelső szintű könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="2ae31-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ae31-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ae31-117">CommonParameters</span></span>
<span data-ttu-id="2ae31-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ae31-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ae31-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ae31-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ae31-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ae31-120">INPUTS</span></span>

### <span data-ttu-id="2ae31-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2ae31-121">System.String</span></span>

### <span data-ttu-id="2ae31-122">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2ae31-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="2ae31-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ae31-123">OUTPUTS</span></span>

### <span data-ttu-id="2ae31-124">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ae31-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="2ae31-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ae31-125">NOTES</span></span>

## <span data-ttu-id="2ae31-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ae31-126">RELATED LINKS</span></span>

[<span data-ttu-id="2ae31-127">Exportálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ae31-127">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2ae31-128">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="2ae31-128">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="2ae31-129">Importálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ae31-129">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2ae31-130">Bekapcsolódás a AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ae31-130">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2ae31-131">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ae31-131">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2ae31-132">Új – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ae31-132">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2ae31-133">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ae31-133">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2ae31-134">Teszt-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ae31-134">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


