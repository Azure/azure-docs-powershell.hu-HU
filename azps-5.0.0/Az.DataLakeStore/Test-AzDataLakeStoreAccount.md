---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297707"
---
# <span data-ttu-id="2fdf3-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2fdf3-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="2fdf3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2fdf3-102">SYNOPSIS</span></span>
<span data-ttu-id="2fdf3-103">Teszteli az adattó áruházbeli fiók létezését.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="2fdf3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2fdf3-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fdf3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2fdf3-105">DESCRIPTION</span></span>
<span data-ttu-id="2fdf3-106">A **teszt-AzDataLakeStoreAccount** parancsmag az Adattó áruházbeli fiók létezését teszteli.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="2fdf3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2fdf3-107">EXAMPLES</span></span>

### <span data-ttu-id="2fdf3-108">Példa 1: fiók tesztelése</span><span class="sxs-lookup"><span data-stu-id="2fdf3-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="2fdf3-109">Ez a parancs azt teszteli, hogy a ContosoADL nevű fiók létezik-e.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="2fdf3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2fdf3-110">PARAMETERS</span></span>

### <span data-ttu-id="2fdf3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fdf3-111">-DefaultProfile</span></span>
<span data-ttu-id="2fdf3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2fdf3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fdf3-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2fdf3-113">-Name</span></span>
<span data-ttu-id="2fdf3-114">A tesztelni kívánt adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="2fdf3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fdf3-115">-ResourceGroupName</span></span>
<span data-ttu-id="2fdf3-116">Annak a csoportnak a neve, amely a tesztelni kívánt fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="2fdf3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fdf3-117">CommonParameters</span></span>
<span data-ttu-id="2fdf3-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2fdf3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fdf3-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fdf3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fdf3-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fdf3-120">INPUTS</span></span>

### <span data-ttu-id="2fdf3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2fdf3-121">System.String</span></span>

## <span data-ttu-id="2fdf3-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fdf3-122">OUTPUTS</span></span>

### <span data-ttu-id="2fdf3-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2fdf3-123">System.Boolean</span></span>

## <span data-ttu-id="2fdf3-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2fdf3-124">NOTES</span></span>

## <span data-ttu-id="2fdf3-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2fdf3-125">RELATED LINKS</span></span>

[<span data-ttu-id="2fdf3-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2fdf3-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="2fdf3-127">Új – AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2fdf3-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="2fdf3-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2fdf3-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="2fdf3-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2fdf3-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


