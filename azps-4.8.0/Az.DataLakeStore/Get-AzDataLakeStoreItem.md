---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017852"
---
# <span data-ttu-id="f1d74-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1d74-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="f1d74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1d74-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d74-103">Az adattó áruházban lévő fájlok vagy mappák részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f1d74-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f1d74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1d74-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1d74-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1d74-105">DESCRIPTION</span></span>
<span data-ttu-id="f1d74-106">A **Get-AzDataLakeStoreItem** parancsmag az adatok tava áruházban található fájlok vagy mappák részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f1d74-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f1d74-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f1d74-107">EXAMPLES</span></span>

### <span data-ttu-id="f1d74-108">1. példa: az adattó áruházból származó fájlok adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="f1d74-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="f1d74-109">Ez a parancs az adattó áruházból Test.csv fájl részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f1d74-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="f1d74-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1d74-110">PARAMETERS</span></span>

### <span data-ttu-id="f1d74-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="f1d74-111">-Account</span></span>
<span data-ttu-id="f1d74-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1d74-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f1d74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d74-113">-DefaultProfile</span></span>
<span data-ttu-id="f1d74-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1d74-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1d74-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="f1d74-115">-Path</span></span>
<span data-ttu-id="f1d74-116">Az adattó-tároló elérési útját adja meg, amelyből egy elem részleteit kapja meg, kezdve a legfelső szintű könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="f1d74-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f1d74-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d74-117">CommonParameters</span></span>
<span data-ttu-id="f1d74-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1d74-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d74-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1d74-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d74-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1d74-120">INPUTS</span></span>

### <span data-ttu-id="f1d74-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f1d74-121">System.String</span></span>

### <span data-ttu-id="f1d74-122">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f1d74-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="f1d74-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1d74-123">OUTPUTS</span></span>

### <span data-ttu-id="f1d74-124">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1d74-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="f1d74-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1d74-125">NOTES</span></span>

## <span data-ttu-id="f1d74-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1d74-126">RELATED LINKS</span></span>

[<span data-ttu-id="f1d74-127">Exportálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1d74-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="f1d74-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="f1d74-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="f1d74-129">Importálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1d74-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="f1d74-130">Bekapcsolódás a AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1d74-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="f1d74-131">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1d74-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="f1d74-132">Új – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1d74-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="f1d74-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1d74-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="f1d74-134">Teszt-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1d74-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


