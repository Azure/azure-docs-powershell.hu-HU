---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.ADDomainServices/new-AzADDomainServiceForestTrust
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
ms.openlocfilehash: aaf3fa74000bd5ab7264386b28fe20588235c951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935913"
---
# <span data-ttu-id="1c72d-101">New-AzADDomainServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="1c72d-101">New-AzADDomainServiceForestTrust</span></span>

## <span data-ttu-id="1c72d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c72d-102">SYNOPSIS</span></span>
<span data-ttu-id="1c72d-103">Create a in-memory object for ForestTrust</span><span class="sxs-lookup"><span data-stu-id="1c72d-103">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="1c72d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1c72d-104">SYNTAX</span></span>

```
New-AzADDomainServiceForestTrust [-FriendlyName <String>] [-RemoteDnsIP <String>] [-TrustDirection <String>]
 [-TrustedDomainFqdn <String>] [-TrustPassword <SecureString>] [<CommonParameters>]
```

## <span data-ttu-id="1c72d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1c72d-105">DESCRIPTION</span></span>
<span data-ttu-id="1c72d-106">Create a in-memory object for ForestTrust</span><span class="sxs-lookup"><span data-stu-id="1c72d-106">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="1c72d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1c72d-107">EXAMPLES</span></span>

### <span data-ttu-id="1c72d-108">1. példa: Create ServiceForestTrust for ADDomain</span><span class="sxs-lookup"><span data-stu-id="1c72d-108">Example 1: Create ServiceForestTrust for ADDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceForestTrust -FriendlyName FriendlyNameTest

FriendlyName     RemoteDnsIP TrustDirection TrustPassword TrustedDomainFqdn
------------     ----------- -------------- ------------- -----------------
FriendlyNameTest
```

<span data-ttu-id="1c72d-109">Create ServiceForestTrust for ADDomain</span><span class="sxs-lookup"><span data-stu-id="1c72d-109">Create ServiceForestTrust for ADDomain</span></span>

## <span data-ttu-id="1c72d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c72d-110">PARAMETERS</span></span>

### <span data-ttu-id="1c72d-111">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1c72d-111">-FriendlyName</span></span>
<span data-ttu-id="1c72d-112">Rövid név.</span><span class="sxs-lookup"><span data-stu-id="1c72d-112">Friendly Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c72d-113">-RemoteDnsIP</span><span class="sxs-lookup"><span data-stu-id="1c72d-113">-RemoteDnsIP</span></span>
<span data-ttu-id="1c72d-114">Távoli DNS-ips.</span><span class="sxs-lookup"><span data-stu-id="1c72d-114">Remote Dns ips.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c72d-115">-TrustDirection</span><span class="sxs-lookup"><span data-stu-id="1c72d-115">-TrustDirection</span></span>
<span data-ttu-id="1c72d-116">Megbízhatósági irány.</span><span class="sxs-lookup"><span data-stu-id="1c72d-116">Trust Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c72d-117">-TrustedDomainFqdn</span><span class="sxs-lookup"><span data-stu-id="1c72d-117">-TrustedDomainFqdn</span></span>
<span data-ttu-id="1c72d-118">Megbízható tartomány teljes tartománynév.</span><span class="sxs-lookup"><span data-stu-id="1c72d-118">Trusted Domain FQDN.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c72d-119">-TrustPassword</span><span class="sxs-lookup"><span data-stu-id="1c72d-119">-TrustPassword</span></span>
<span data-ttu-id="1c72d-120">Megbízható jelszó.</span><span class="sxs-lookup"><span data-stu-id="1c72d-120">Trust Password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c72d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c72d-121">CommonParameters</span></span>
<span data-ttu-id="1c72d-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c72d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c72d-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c72d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c72d-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c72d-124">INPUTS</span></span>

## <span data-ttu-id="1c72d-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c72d-125">OUTPUTS</span></span>

### <span data-ttu-id="1c72d-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span><span class="sxs-lookup"><span data-stu-id="1c72d-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span></span>

## <span data-ttu-id="1c72d-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1c72d-127">NOTES</span></span>

<span data-ttu-id="1c72d-128">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1c72d-128">ALIASES</span></span>

## <span data-ttu-id="1c72d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c72d-129">RELATED LINKS</span></span>

