---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: c78ad67e884eeac1cc6f4b589fd15e0493ee738a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209646"
---
# <span data-ttu-id="8a299-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="8a299-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="8a299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a299-102">SYNOPSIS</span></span>
<span data-ttu-id="8a299-103">Memóriában létrehozott objektum létrehozása a DigitalTwinsIdentity alkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="8a299-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="8a299-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8a299-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="8a299-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8a299-105">DESCRIPTION</span></span>
<span data-ttu-id="8a299-106">Create a in-memory object for DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="8a299-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="8a299-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8a299-107">EXAMPLES</span></span>

### <span data-ttu-id="8a299-108">1. példa: DigitalTwinsIdentityObject létrehozása</span><span class="sxs-lookup"><span data-stu-id="8a299-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="8a299-109">DigitalTwinsIdentityObject létrehozása azonosító és hely alapján</span><span class="sxs-lookup"><span data-stu-id="8a299-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="8a299-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a299-110">PARAMETERS</span></span>

### <span data-ttu-id="8a299-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8a299-111">-EndpointName</span></span>
<span data-ttu-id="8a299-112">A végponterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8a299-112">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="8a299-113">-Id</span><span class="sxs-lookup"><span data-stu-id="8a299-113">-Id</span></span>
<span data-ttu-id="8a299-114">Erőforrás-identitás elérési útja.</span><span class="sxs-lookup"><span data-stu-id="8a299-114">Resource identity path.</span></span>

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

### <span data-ttu-id="8a299-115">-Location</span><span class="sxs-lookup"><span data-stu-id="8a299-115">-Location</span></span>
<span data-ttu-id="8a299-116">A DigitalTwinsInstance helye.</span><span class="sxs-lookup"><span data-stu-id="8a299-116">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="8a299-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a299-117">-ResourceGroupName</span></span>
<span data-ttu-id="8a299-118">A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8a299-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="8a299-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8a299-119">-ResourceName</span></span>
<span data-ttu-id="8a299-120">A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="8a299-120">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="8a299-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a299-121">-SubscriptionId</span></span>
<span data-ttu-id="8a299-122">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8a299-122">The subscription identifier.</span></span>

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

### <span data-ttu-id="8a299-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a299-123">CommonParameters</span></span>
<span data-ttu-id="8a299-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a299-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a299-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a299-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a299-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a299-126">INPUTS</span></span>

## <span data-ttu-id="8a299-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a299-127">OUTPUTS</span></span>

### <span data-ttu-id="8a299-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="8a299-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="8a299-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8a299-129">NOTES</span></span>

<span data-ttu-id="8a299-130">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8a299-130">ALIASES</span></span>

## <span data-ttu-id="8a299-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a299-131">RELATED LINKS</span></span>

