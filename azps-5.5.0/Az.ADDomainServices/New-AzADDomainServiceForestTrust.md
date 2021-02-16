---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.ADDomainServices/new-AzADDomainServiceForestTrust
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
ms.openlocfilehash: 91d7b92b7b52df20d69f53cddb98d6b9276b0b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143827"
---
# <span data-ttu-id="b9440-101">New-AzADDomainServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="b9440-101">New-AzADDomainServiceForestTrust</span></span>

## <span data-ttu-id="b9440-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9440-102">SYNOPSIS</span></span>
<span data-ttu-id="b9440-103">Create a in-memory object for ForestTrust</span><span class="sxs-lookup"><span data-stu-id="b9440-103">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="b9440-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b9440-104">SYNTAX</span></span>

```
New-AzADDomainServiceForestTrust [-FriendlyName <String>] [-RemoteDnsIP <String>] [-TrustDirection <String>]
 [-TrustedDomainFqdn <String>] [-TrustPassword <SecureString>] [<CommonParameters>]
```

## <span data-ttu-id="b9440-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b9440-105">DESCRIPTION</span></span>
<span data-ttu-id="b9440-106">Memóriában található objektum létrehozása a ForestTrust számára</span><span class="sxs-lookup"><span data-stu-id="b9440-106">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="b9440-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b9440-107">EXAMPLES</span></span>

### <span data-ttu-id="b9440-108">1. példa: Create ServiceForestTrust for ADDomain</span><span class="sxs-lookup"><span data-stu-id="b9440-108">Example 1: Create ServiceForestTrust for ADDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceForestTrust -FriendlyName FriendlyNameTest

FriendlyName     RemoteDnsIP TrustDirection TrustPassword TrustedDomainFqdn
------------     ----------- -------------- ------------- -----------------
FriendlyNameTest
```

<span data-ttu-id="b9440-109">Create ServiceForestTrust for ADDomain</span><span class="sxs-lookup"><span data-stu-id="b9440-109">Create ServiceForestTrust for ADDomain</span></span>

## <span data-ttu-id="b9440-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9440-110">PARAMETERS</span></span>

### <span data-ttu-id="b9440-111">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b9440-111">-FriendlyName</span></span>
<span data-ttu-id="b9440-112">Rövid név.</span><span class="sxs-lookup"><span data-stu-id="b9440-112">Friendly Name.</span></span>

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

### <span data-ttu-id="b9440-113">-RemoteDnsIP</span><span class="sxs-lookup"><span data-stu-id="b9440-113">-RemoteDnsIP</span></span>
<span data-ttu-id="b9440-114">Távoli DNS-ips.</span><span class="sxs-lookup"><span data-stu-id="b9440-114">Remote Dns ips.</span></span>

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

### <span data-ttu-id="b9440-115">-TrustDirection</span><span class="sxs-lookup"><span data-stu-id="b9440-115">-TrustDirection</span></span>
<span data-ttu-id="b9440-116">Megbízhatósági irány.</span><span class="sxs-lookup"><span data-stu-id="b9440-116">Trust Direction.</span></span>

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

### <span data-ttu-id="b9440-117">-TrustedDomainFqdn</span><span class="sxs-lookup"><span data-stu-id="b9440-117">-TrustedDomainFqdn</span></span>
<span data-ttu-id="b9440-118">Megbízható tartomány teljes tartománynév.</span><span class="sxs-lookup"><span data-stu-id="b9440-118">Trusted Domain FQDN.</span></span>

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

### <span data-ttu-id="b9440-119">-TrustPassword</span><span class="sxs-lookup"><span data-stu-id="b9440-119">-TrustPassword</span></span>
<span data-ttu-id="b9440-120">Megbízható jelszó.</span><span class="sxs-lookup"><span data-stu-id="b9440-120">Trust Password.</span></span>

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

### <span data-ttu-id="b9440-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9440-121">CommonParameters</span></span>
<span data-ttu-id="b9440-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9440-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9440-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9440-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9440-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9440-124">INPUTS</span></span>

## <span data-ttu-id="b9440-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9440-125">OUTPUTS</span></span>

### <span data-ttu-id="b9440-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span><span class="sxs-lookup"><span data-stu-id="b9440-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span></span>

## <span data-ttu-id="b9440-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b9440-127">NOTES</span></span>

<span data-ttu-id="b9440-128">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b9440-128">ALIASES</span></span>

## <span data-ttu-id="b9440-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9440-129">RELATED LINKS</span></span>

