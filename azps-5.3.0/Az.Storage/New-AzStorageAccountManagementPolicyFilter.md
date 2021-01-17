---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 48ae8b87671e52abe4d109025048fe1e4aeca117
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469273"
---
# <span data-ttu-id="ec877-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ec877-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="ec877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec877-102">SYNOPSIS</span></span>
<span data-ttu-id="ec877-103">Létrehoz egy ManagementPolicy szabályszűrő objektumot, amely használható a New-AzStorageAccountManagementPolicyRule-ban.</span><span class="sxs-lookup"><span data-stu-id="ec877-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="ec877-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ec877-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec877-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ec877-105">DESCRIPTION</span></span>
<span data-ttu-id="ec877-106">A **New-AzStorageAccountManagementPolicyFilter** parancsmag létrehoz egy ManagementPolicy szabályszűrő objektumot, amely használható a New-AzStorageAccountManagementPolicyRule-ban.</span><span class="sxs-lookup"><span data-stu-id="ec877-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="ec877-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ec877-107">EXAMPLES</span></span>

### <span data-ttu-id="ec877-108">1. példa: Létrehoz egy ManagementPolicy szabályszűrő objektumot, majd hozzáadja egy felügyeleti házirendszabályhoz, és tárhelyfiókra van állítva</span><span class="sxs-lookup"><span data-stu-id="ec877-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="ec877-109">Ez a parancs Létrehoz egy ManagementPolicy szabályszűrő objektumot.</span><span class="sxs-lookup"><span data-stu-id="ec877-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="ec877-110">Ezután vegye fel egy felügyeleti házirendszabályba, és állítsa be tárfiókként.</span><span class="sxs-lookup"><span data-stu-id="ec877-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="ec877-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec877-111">PARAMETERS</span></span>

### <span data-ttu-id="ec877-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec877-112">-DefaultProfile</span></span>
<span data-ttu-id="ec877-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec877-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec877-114">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="ec877-114">-PrefixMatch</span></span>
<span data-ttu-id="ec877-115">Az előtagok egyező karakterláncokat tartalmazó tömbje.</span><span class="sxs-lookup"><span data-stu-id="ec877-115">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="ec877-116">Az előtag karakterláncának egy tárolónévvel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="ec877-116">A prefix string must start with a container name.</span></span>

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

### <span data-ttu-id="ec877-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec877-117">CommonParameters</span></span>
<span data-ttu-id="ec877-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec877-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec877-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec877-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec877-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec877-120">INPUTS</span></span>

### <span data-ttu-id="ec877-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="ec877-121">None</span></span>

## <span data-ttu-id="ec877-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec877-122">OUTPUTS</span></span>

### <span data-ttu-id="ec877-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="ec877-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="ec877-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ec877-124">NOTES</span></span>

## <span data-ttu-id="ec877-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec877-125">RELATED LINKS</span></span>
