---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 8bc8a09add012cb0f190922777e2e9e7fcc46feb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941202"
---
# <span data-ttu-id="3896d-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3896d-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="3896d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3896d-102">SYNOPSIS</span></span>
<span data-ttu-id="3896d-103">Teszteli egy Data Lake Store-fiók meglétét.</span><span class="sxs-lookup"><span data-stu-id="3896d-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="3896d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3896d-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3896d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3896d-105">DESCRIPTION</span></span>
<span data-ttu-id="3896d-106">A **Test-AzDataLakeStoreAccount** parancsmag teszteli a Data Lake Store-fiók meglétét.</span><span class="sxs-lookup"><span data-stu-id="3896d-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="3896d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3896d-107">EXAMPLES</span></span>

### <span data-ttu-id="3896d-108">1. példa: Fiók tesztelése</span><span class="sxs-lookup"><span data-stu-id="3896d-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="3896d-109">Ez a parancs teszteli, hogy létezik-e a ContosoADL nevű fiók.</span><span class="sxs-lookup"><span data-stu-id="3896d-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="3896d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3896d-110">PARAMETERS</span></span>

### <span data-ttu-id="3896d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3896d-111">-DefaultProfile</span></span>
<span data-ttu-id="3896d-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3896d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3896d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3896d-113">-Name</span></span>
<span data-ttu-id="3896d-114">A tesztelni szükséges Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3896d-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="3896d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3896d-115">-ResourceGroupName</span></span>
<span data-ttu-id="3896d-116">Annak az erőforráscsoportnak a nevét adja meg, amely a tesztelni kívánt fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3896d-116">Specifies the name of the resource group that contains the account to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3896d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3896d-117">CommonParameters</span></span>
<span data-ttu-id="3896d-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3896d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3896d-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3896d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3896d-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3896d-120">INPUTS</span></span>

### <span data-ttu-id="3896d-121">System.String</span><span class="sxs-lookup"><span data-stu-id="3896d-121">System.String</span></span>

## <span data-ttu-id="3896d-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3896d-122">OUTPUTS</span></span>

### <span data-ttu-id="3896d-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3896d-123">System.Boolean</span></span>

## <span data-ttu-id="3896d-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3896d-124">NOTES</span></span>

## <span data-ttu-id="3896d-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3896d-125">RELATED LINKS</span></span>

[<span data-ttu-id="3896d-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3896d-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="3896d-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3896d-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="3896d-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3896d-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="3896d-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3896d-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


