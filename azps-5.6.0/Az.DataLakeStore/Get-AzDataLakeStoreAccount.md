---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 845fbb645ca9ba3495aa0dcf2b56cdbd793630e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924162"
---
# <span data-ttu-id="c79fd-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c79fd-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="c79fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c79fd-102">SYNOPSIS</span></span>
<span data-ttu-id="c79fd-103">Részleteket kap egy Data Lake Store-fiókról.</span><span class="sxs-lookup"><span data-stu-id="c79fd-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="c79fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c79fd-104">SYNTAX</span></span>

### <span data-ttu-id="c79fd-105">GetAllInSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c79fd-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c79fd-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c79fd-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c79fd-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="c79fd-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c79fd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c79fd-108">DESCRIPTION</span></span>
<span data-ttu-id="c79fd-109">A **Get-AzDataLakeStoreAccount** parancsmag részleteket kap egy Data Lake Store-fiókról.</span><span class="sxs-lookup"><span data-stu-id="c79fd-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="c79fd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c79fd-110">EXAMPLES</span></span>

### <span data-ttu-id="c79fd-111">1. példa: Data Lake Store-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="c79fd-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="c79fd-112">Ez a parancs a ContosoADL nevű fiókot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c79fd-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="c79fd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c79fd-113">PARAMETERS</span></span>

### <span data-ttu-id="c79fd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c79fd-114">-DefaultProfile</span></span>
<span data-ttu-id="c79fd-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c79fd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c79fd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c79fd-116">-Name</span></span>
<span data-ttu-id="c79fd-117">A lekért fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c79fd-117">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79fd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c79fd-118">-ResourceGroupName</span></span>
<span data-ttu-id="c79fd-119">Annak az erőforráscsoportnak a neve, amely a lekért Data Lake Store-fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c79fd-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79fd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c79fd-120">CommonParameters</span></span>
<span data-ttu-id="c79fd-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c79fd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c79fd-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c79fd-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c79fd-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c79fd-123">INPUTS</span></span>

### <span data-ttu-id="c79fd-124">System.String</span><span class="sxs-lookup"><span data-stu-id="c79fd-124">System.String</span></span>

## <span data-ttu-id="c79fd-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c79fd-125">OUTPUTS</span></span>

### <span data-ttu-id="c79fd-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c79fd-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="c79fd-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c79fd-127">NOTES</span></span>

## <span data-ttu-id="c79fd-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c79fd-128">RELATED LINKS</span></span>

[<span data-ttu-id="c79fd-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c79fd-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="c79fd-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c79fd-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="c79fd-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c79fd-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="c79fd-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c79fd-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


