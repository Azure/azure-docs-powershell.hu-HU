---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: 2662eeeeaedbac75f443bf6160c625dfdb8dd854
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372972"
---
# <span data-ttu-id="85d94-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="85d94-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="85d94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85d94-102">SYNOPSIS</span></span>
<span data-ttu-id="85d94-103">Egy Batch-fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="85d94-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="85d94-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="85d94-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85d94-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="85d94-105">DESCRIPTION</span></span>
<span data-ttu-id="85d94-106">A **Get-AzBatchAccountKey** parancsmag az aktuális előfizetésben lévő Azure Batch-fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="85d94-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="85d94-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="85d94-107">EXAMPLES</span></span>

### <span data-ttu-id="85d94-108">1. példa: Kötegelt fiókkulcsok lekérte és egy változóba mentve $Context későbbi használatra</span><span class="sxs-lookup"><span data-stu-id="85d94-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="85d94-109">Ez a parancs lekérte a fiók adatait, és egy objektumban tárolja későbbi `$Context` használatra.</span><span class="sxs-lookup"><span data-stu-id="85d94-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="85d94-110">2. példa: A kötegfiók kulcsának be- és megjelenítése</span><span class="sxs-lookup"><span data-stu-id="85d94-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="85d94-111">Ez a parancs beveszi a fiókkulcsokat, és kinyomtatja őket a konzolra.</span><span class="sxs-lookup"><span data-stu-id="85d94-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="85d94-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85d94-112">PARAMETERS</span></span>

### <span data-ttu-id="85d94-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="85d94-113">-AccountName</span></span>
<span data-ttu-id="85d94-114">Annak a fióknak a nevét adja meg, amelyhez a parancsmag kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="85d94-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="85d94-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85d94-115">-DefaultProfile</span></span>
<span data-ttu-id="85d94-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85d94-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85d94-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85d94-117">-ResourceGroupName</span></span>
<span data-ttu-id="85d94-118">Annak az erőforráscsoportnak a nevét adja meg, amely azt a fiókot tartalmazza, amelyhez a parancsmag kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="85d94-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="85d94-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85d94-119">CommonParameters</span></span>
<span data-ttu-id="85d94-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85d94-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85d94-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85d94-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85d94-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85d94-122">INPUTS</span></span>

### <span data-ttu-id="85d94-123">System.String</span><span class="sxs-lookup"><span data-stu-id="85d94-123">System.String</span></span>

## <span data-ttu-id="85d94-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85d94-124">OUTPUTS</span></span>

### <span data-ttu-id="85d94-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="85d94-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="85d94-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="85d94-126">NOTES</span></span>

## <span data-ttu-id="85d94-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85d94-127">RELATED LINKS</span></span>

[<span data-ttu-id="85d94-128">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="85d94-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="85d94-129">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="85d94-129">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
