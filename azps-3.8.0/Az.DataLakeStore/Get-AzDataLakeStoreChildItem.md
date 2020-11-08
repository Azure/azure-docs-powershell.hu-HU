---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 6123cacd35eb0a683ec2103ea00e2e06a2d80cd2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010504"
---
# <span data-ttu-id="ee156-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="ee156-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="ee156-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee156-102">SYNOPSIS</span></span>
<span data-ttu-id="ee156-103">Az elemek listájának beolvasása az adattó áruházban lévő mappákban.</span><span class="sxs-lookup"><span data-stu-id="ee156-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="ee156-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee156-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee156-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee156-105">DESCRIPTION</span></span>
<span data-ttu-id="ee156-106">A **Get-AzDataLakeStoreChildItem** parancsmag az adattó-tárolóban lévő elemek listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ee156-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="ee156-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ee156-107">EXAMPLES</span></span>

### <span data-ttu-id="ee156-108">Példa 1: egy mappa alárendelt elemeinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="ee156-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="ee156-109">Ez a parancs beolvassa a MyFiles mappa alárendelt elemeit.</span><span class="sxs-lookup"><span data-stu-id="ee156-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="ee156-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee156-110">PARAMETERS</span></span>

### <span data-ttu-id="ee156-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="ee156-111">-Account</span></span>
<span data-ttu-id="ee156-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee156-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ee156-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee156-113">-DefaultProfile</span></span>
<span data-ttu-id="ee156-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee156-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee156-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="ee156-115">-Path</span></span>
<span data-ttu-id="ee156-116">A mappa Data Lake Store elérési útját adja meg a gyökérkönyvtártól (/) kezdve.</span><span class="sxs-lookup"><span data-stu-id="ee156-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ee156-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee156-117">CommonParameters</span></span>
<span data-ttu-id="ee156-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee156-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee156-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee156-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee156-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee156-120">INPUTS</span></span>

### <span data-ttu-id="ee156-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ee156-121">System.String</span></span>

### <span data-ttu-id="ee156-122">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="ee156-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="ee156-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee156-123">OUTPUTS</span></span>

### <span data-ttu-id="ee156-124">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ee156-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="ee156-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee156-125">NOTES</span></span>

## <span data-ttu-id="ee156-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee156-126">RELATED LINKS</span></span>
