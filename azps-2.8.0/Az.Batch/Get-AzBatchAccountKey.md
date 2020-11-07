---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: a9289bc6a0db4403b96e982fd28f91578e3a0c9b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847861"
---
# <span data-ttu-id="e2959-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e2959-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="e2959-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2959-102">SYNOPSIS</span></span>
<span data-ttu-id="e2959-103">Egy köteg fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e2959-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="e2959-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2959-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2959-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2959-105">DESCRIPTION</span></span>
<span data-ttu-id="e2959-106">A **Get-AzBatchAccountKey** parancsmag az Azure-kötegek kulcsait az aktuális előfizetésben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e2959-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="e2959-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e2959-107">EXAMPLES</span></span>

### <span data-ttu-id="e2959-108">Példa 1: a kötegelt fiók kulcsainak beolvasása és mentése $Context változóban későbbi használatra</span><span class="sxs-lookup"><span data-stu-id="e2959-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="e2959-109">Ez a parancs a fiók adatait az objektumba menti, majd `$Context` később használatba veszi.</span><span class="sxs-lookup"><span data-stu-id="e2959-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="e2959-110">2. példa: a kötegelt fiók gombjainak beolvasása és megjelenítése</span><span class="sxs-lookup"><span data-stu-id="e2959-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="e2959-111">Ez a parancs megkapja a fiók kulcsait, és kinyomtatja őket a konzolra.</span><span class="sxs-lookup"><span data-stu-id="e2959-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="e2959-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2959-112">PARAMETERS</span></span>

### <span data-ttu-id="e2959-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e2959-113">-AccountName</span></span>
<span data-ttu-id="e2959-114">Annak a fióknak a nevét adja meg, amelynek a parancsmagja kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="e2959-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2959-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2959-115">-DefaultProfile</span></span>
<span data-ttu-id="e2959-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2959-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2959-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2959-117">-ResourceGroupName</span></span>
<span data-ttu-id="e2959-118">Annak a fióknak a nevét adja meg az erőforráscsoport számára, amelynek a parancsmagja kulcsokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e2959-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2959-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2959-119">CommonParameters</span></span>
<span data-ttu-id="e2959-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2959-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2959-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2959-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2959-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2959-122">INPUTS</span></span>

### <span data-ttu-id="e2959-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e2959-123">System.String</span></span>

## <span data-ttu-id="e2959-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2959-124">OUTPUTS</span></span>

### <span data-ttu-id="e2959-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e2959-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e2959-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2959-126">NOTES</span></span>

## <span data-ttu-id="e2959-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2959-127">RELATED LINKS</span></span>

[<span data-ttu-id="e2959-128">Új – AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e2959-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="e2959-129">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e2959-129">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

