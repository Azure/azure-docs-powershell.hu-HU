---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465781"
---
# <span data-ttu-id="3d93b-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3d93b-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="3d93b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d93b-102">SYNOPSIS</span></span>
<span data-ttu-id="3d93b-103">Teszteli egy Data Lake Store-fiók meglétét.</span><span class="sxs-lookup"><span data-stu-id="3d93b-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="3d93b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3d93b-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d93b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3d93b-105">DESCRIPTION</span></span>
<span data-ttu-id="3d93b-106">A **Test-AzDataLakeStoreAccount** parancsmag teszteli a Data Lake Store-fiók meglétét.</span><span class="sxs-lookup"><span data-stu-id="3d93b-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="3d93b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3d93b-107">EXAMPLES</span></span>

### <span data-ttu-id="3d93b-108">1. példa: Fiók tesztelése</span><span class="sxs-lookup"><span data-stu-id="3d93b-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="3d93b-109">Ez a parancs teszteli, hogy létezik-e a ContosoADL nevű fiók.</span><span class="sxs-lookup"><span data-stu-id="3d93b-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="3d93b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d93b-110">PARAMETERS</span></span>

### <span data-ttu-id="3d93b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d93b-111">-DefaultProfile</span></span>
<span data-ttu-id="3d93b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3d93b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d93b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3d93b-113">-Name</span></span>
<span data-ttu-id="3d93b-114">A tesztelni szükséges Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d93b-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="3d93b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d93b-115">-ResourceGroupName</span></span>
<span data-ttu-id="3d93b-116">Annak az erőforráscsoportnak a nevét adja meg, amely a tesztelni kívánt fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3d93b-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="3d93b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d93b-117">CommonParameters</span></span>
<span data-ttu-id="3d93b-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d93b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d93b-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d93b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d93b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d93b-120">INPUTS</span></span>

### <span data-ttu-id="3d93b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="3d93b-121">System.String</span></span>

## <span data-ttu-id="3d93b-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d93b-122">OUTPUTS</span></span>

### <span data-ttu-id="3d93b-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3d93b-123">System.Boolean</span></span>

## <span data-ttu-id="3d93b-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3d93b-124">NOTES</span></span>

## <span data-ttu-id="3d93b-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d93b-125">RELATED LINKS</span></span>

[<span data-ttu-id="3d93b-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3d93b-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="3d93b-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3d93b-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="3d93b-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3d93b-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="3d93b-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3d93b-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


