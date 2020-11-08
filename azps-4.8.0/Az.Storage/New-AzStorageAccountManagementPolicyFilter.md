---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 48ae8b87671e52abe4d109025048fe1e4aeca117
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183802"
---
# <span data-ttu-id="8f5c6-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="8f5c6-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="8f5c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f5c6-102">SYNOPSIS</span></span>
<span data-ttu-id="8f5c6-103">Létrehoz egy ManagementPolicy-szabályt, amely a New-AzStorageAccountManagementPolicyRule is használható.</span><span class="sxs-lookup"><span data-stu-id="8f5c6-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="8f5c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f5c6-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f5c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f5c6-105">DESCRIPTION</span></span>
<span data-ttu-id="8f5c6-106">A **New-AzStorageAccountManagementPolicyFilter** parancsmag létrehoz egy ManagementPolicy-szabályt, amely a New-AzStorageAccountManagementPolicyRule is használható.</span><span class="sxs-lookup"><span data-stu-id="8f5c6-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="8f5c6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8f5c6-107">EXAMPLES</span></span>

### <span data-ttu-id="8f5c6-108">Példa 1: ManagementPolicy-szűrő objektum létrehozása, majd felvétele felügyeleti házirend-szabályba, és beállítása tárolási fiókra</span><span class="sxs-lookup"><span data-stu-id="8f5c6-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
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

<span data-ttu-id="8f5c6-109">Ezzel a paranccsal létrehozhatja a ManagementPolicy objektumát.</span><span class="sxs-lookup"><span data-stu-id="8f5c6-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="8f5c6-110">Ezután adja hozzá egy felügyeleti házirend-szabályhoz, és állítsa be a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="8f5c6-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="8f5c6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f5c6-111">PARAMETERS</span></span>

### <span data-ttu-id="8f5c6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f5c6-112">-DefaultProfile</span></span>
<span data-ttu-id="8f5c6-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f5c6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f5c6-114">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="8f5c6-114">-PrefixMatch</span></span>
<span data-ttu-id="8f5c6-115">Az ELŐTAGOKNAK megfelelő karakterláncokat tartalmazó tömb.</span><span class="sxs-lookup"><span data-stu-id="8f5c6-115">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="8f5c6-116">Az előtag-karakterláncnak tároló névvel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="8f5c6-116">A prefix string must start with a container name.</span></span>

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

### <span data-ttu-id="8f5c6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f5c6-117">CommonParameters</span></span>
<span data-ttu-id="8f5c6-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f5c6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f5c6-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f5c6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f5c6-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f5c6-120">INPUTS</span></span>

### <span data-ttu-id="8f5c6-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="8f5c6-121">None</span></span>

## <span data-ttu-id="8f5c6-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f5c6-122">OUTPUTS</span></span>

### <span data-ttu-id="8f5c6-123">Microsoft. Azure. Command. Management. Storage. models. PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="8f5c6-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="8f5c6-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f5c6-124">NOTES</span></span>

## <span data-ttu-id="8f5c6-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f5c6-125">RELATED LINKS</span></span>
