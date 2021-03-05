---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 40a2420803197b21bb9f0f8d20b771482b4e694b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002630"
---
# <span data-ttu-id="c16da-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="c16da-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="c16da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c16da-102">SYNOPSIS</span></span>
<span data-ttu-id="c16da-103">Létrehoz egy ManagementPolicy szabályszűrő objektumot, amely használható a New-AzStorageAccountManagementPolicyRule-ban.</span><span class="sxs-lookup"><span data-stu-id="c16da-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="c16da-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c16da-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-BlobType <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c16da-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c16da-105">DESCRIPTION</span></span>
<span data-ttu-id="c16da-106">A **New-AzStorageAccountManagementPolicyFilter** parancsmag létrehoz egy ManagementPolicy szabályszűrő objektumot, amely használható a New-AzStorageAccountManagementPolicyRule-ban.</span><span class="sxs-lookup"><span data-stu-id="c16da-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="c16da-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c16da-107">EXAMPLES</span></span>

### <span data-ttu-id="c16da-108">1. példa: Létrehoz egy ManagementPolicy szabályszűrő objektumot, majd hozzáadja egy felügyeleti házirendszabályhoz, és tárhelyfiókra van állítva</span><span class="sxs-lookup"><span data-stu-id="c16da-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2 -BlobType appendBlob,blockBlob
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {appendBlob, blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="c16da-109">Ez a parancs Létrehoz egy ManagementPolicy szabályszűrő objektumot.</span><span class="sxs-lookup"><span data-stu-id="c16da-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="c16da-110">Ezután vegye fel egy felügyeleti házirendszabályba, és állítsa be tárfiókként.</span><span class="sxs-lookup"><span data-stu-id="c16da-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="c16da-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c16da-111">PARAMETERS</span></span>

### <span data-ttu-id="c16da-112">-BlobType</span><span class="sxs-lookup"><span data-stu-id="c16da-112">-BlobType</span></span>
<span data-ttu-id="c16da-113">A blobtípusoknak megfelelő karakterláncok tömbje.</span><span class="sxs-lookup"><span data-stu-id="c16da-113">An array of strings for blobtypes to be match.</span></span> <span data-ttu-id="c16da-114">A blockBlob jelenleg az összes rétegezési és törlési műveletet támogatja.</span><span class="sxs-lookup"><span data-stu-id="c16da-114">Currently blockBlob supports all tiering and delete actions.</span></span> <span data-ttu-id="c16da-115">A appendBlob csak a törlési műveleteket támogatja.</span><span class="sxs-lookup"><span data-stu-id="c16da-115">Only delete actions are supported for appendBlob.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: blockBlob, appendBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c16da-116">-DefaultProfile</span></span>
<span data-ttu-id="c16da-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c16da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c16da-118">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="c16da-118">-PrefixMatch</span></span>
<span data-ttu-id="c16da-119">Az előtagok egyező karakterláncokat tartalmazó tömbje.</span><span class="sxs-lookup"><span data-stu-id="c16da-119">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="c16da-120">Az előtag karakterláncának egy tárolónévvel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="c16da-120">A prefix string must start with a container name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c16da-121">CommonParameters</span></span>
<span data-ttu-id="c16da-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c16da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c16da-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c16da-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c16da-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c16da-124">INPUTS</span></span>

### <span data-ttu-id="c16da-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="c16da-125">None</span></span>

## <span data-ttu-id="c16da-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c16da-126">OUTPUTS</span></span>

### <span data-ttu-id="c16da-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="c16da-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="c16da-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c16da-128">NOTES</span></span>

## <span data-ttu-id="c16da-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c16da-129">RELATED LINKS</span></span>
