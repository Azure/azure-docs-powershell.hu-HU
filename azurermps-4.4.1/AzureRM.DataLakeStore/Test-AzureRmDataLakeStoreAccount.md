---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 8aeb682b270de821a6944c619d7933148b2855e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505071"
---
# <span data-ttu-id="c9309-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c9309-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="c9309-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9309-102">SYNOPSIS</span></span>
<span data-ttu-id="c9309-103">Teszteli az adattó áruházbeli fiók létezését.</span><span class="sxs-lookup"><span data-stu-id="c9309-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9309-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9309-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9309-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9309-105">DESCRIPTION</span></span>
<span data-ttu-id="c9309-106">A **teszt-AzureRmDataLakeStoreAccount** parancsmag az Adattó áruházbeli fiók létezését teszteli.</span><span class="sxs-lookup"><span data-stu-id="c9309-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="c9309-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c9309-107">EXAMPLES</span></span>

### <span data-ttu-id="c9309-108">Példa 1: fiók tesztelése</span><span class="sxs-lookup"><span data-stu-id="c9309-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="c9309-109">Ez a parancs azt teszteli, hogy a ContosoADL nevű fiók létezik-e.</span><span class="sxs-lookup"><span data-stu-id="c9309-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="c9309-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9309-110">PARAMETERS</span></span>

### <span data-ttu-id="c9309-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c9309-111">-Name</span></span>
<span data-ttu-id="c9309-112">A tesztelni kívánt adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9309-112">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="c9309-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9309-113">-ResourceGroupName</span></span>
<span data-ttu-id="c9309-114">Annak a csoportnak a neve, amely a tesztelni kívánt fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c9309-114">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="c9309-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9309-115">-DefaultProfile</span></span>
<span data-ttu-id="c9309-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9309-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9309-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9309-117">CommonParameters</span></span>
<span data-ttu-id="c9309-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9309-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9309-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9309-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9309-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9309-120">INPUTS</span></span>

## <span data-ttu-id="c9309-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9309-121">OUTPUTS</span></span>

### <span data-ttu-id="c9309-122">bool</span><span class="sxs-lookup"><span data-stu-id="c9309-122">bool</span></span>
<span data-ttu-id="c9309-123">Igaz vagy hamis: a megadott fiók létezését jelzi.</span><span class="sxs-lookup"><span data-stu-id="c9309-123">True or false indicating the existence of the specified account.</span></span>

## <span data-ttu-id="c9309-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9309-124">NOTES</span></span>

## <span data-ttu-id="c9309-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9309-125">RELATED LINKS</span></span>

[<span data-ttu-id="c9309-126">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c9309-126">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c9309-127">Új – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c9309-127">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c9309-128">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c9309-128">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c9309-129">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c9309-129">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


