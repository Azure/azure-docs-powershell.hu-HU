---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: 2b038699dfa1cd959ea20b761b6c24dee69a9e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935138"
---
# <span data-ttu-id="6f86c-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="6f86c-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="6f86c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f86c-102">SYNOPSIS</span></span>
<span data-ttu-id="6f86c-103">Memóriában létrehozott objektum létrehozása a DigitalTwinsIdentity alkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="6f86c-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="6f86c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6f86c-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="6f86c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6f86c-105">DESCRIPTION</span></span>
<span data-ttu-id="6f86c-106">Memóriában létrehozott objektum létrehozása a DigitalTwinsIdentity alkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="6f86c-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="6f86c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6f86c-107">EXAMPLES</span></span>

### <span data-ttu-id="6f86c-108">1. példa: DigitalTwinsIdentityObject létrehozása</span><span class="sxs-lookup"><span data-stu-id="6f86c-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="6f86c-109">DigitalTwinsIdentityObject létrehozása azonosító és hely alapján</span><span class="sxs-lookup"><span data-stu-id="6f86c-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="6f86c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f86c-110">PARAMETERS</span></span>

### <span data-ttu-id="6f86c-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6f86c-111">-EndpointName</span></span>
<span data-ttu-id="6f86c-112">A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6f86c-112">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="6f86c-113">-Id</span><span class="sxs-lookup"><span data-stu-id="6f86c-113">-Id</span></span>
<span data-ttu-id="6f86c-114">Erőforrás-identitás elérési útja.</span><span class="sxs-lookup"><span data-stu-id="6f86c-114">Resource identity path.</span></span>

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

### <span data-ttu-id="6f86c-115">-Location</span><span class="sxs-lookup"><span data-stu-id="6f86c-115">-Location</span></span>
<span data-ttu-id="6f86c-116">A DigitalTwinsInstance helye.</span><span class="sxs-lookup"><span data-stu-id="6f86c-116">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="6f86c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f86c-117">-ResourceGroupName</span></span>
<span data-ttu-id="6f86c-118">A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6f86c-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="6f86c-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6f86c-119">-ResourceName</span></span>
<span data-ttu-id="6f86c-120">A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="6f86c-120">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="6f86c-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6f86c-121">-SubscriptionId</span></span>
<span data-ttu-id="6f86c-122">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6f86c-122">The subscription identifier.</span></span>

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

### <span data-ttu-id="6f86c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f86c-123">CommonParameters</span></span>
<span data-ttu-id="6f86c-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f86c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f86c-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f86c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f86c-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f86c-126">INPUTS</span></span>

## <span data-ttu-id="6f86c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f86c-127">OUTPUTS</span></span>

### <span data-ttu-id="6f86c-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="6f86c-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="6f86c-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6f86c-129">NOTES</span></span>

<span data-ttu-id="6f86c-130">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6f86c-130">ALIASES</span></span>

## <span data-ttu-id="6f86c-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f86c-131">RELATED LINKS</span></span>

