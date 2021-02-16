---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: dab6388205c00ee457b7f8095f0f529f591b304f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145355"
---
# <span data-ttu-id="95c62-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="95c62-101">Get-AzContext</span></span>

## <span data-ttu-id="95c62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95c62-102">SYNOPSIS</span></span>
<span data-ttu-id="95c62-103">Az Azure Resource Manager-kérelmek hitelesítéséhez használt metaadatok bekérése.</span><span class="sxs-lookup"><span data-stu-id="95c62-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="95c62-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="95c62-104">SYNTAX</span></span>

### <span data-ttu-id="95c62-105">GetSingleContext (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="95c62-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="95c62-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="95c62-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95c62-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="95c62-107">DESCRIPTION</span></span>
<span data-ttu-id="95c62-108">A Get-AzContext parancsmag megkapja az Azure Resource Manager-kérelmek hitelesítéséhez használt aktuális metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="95c62-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="95c62-109">Ez a parancsmag az Active Directory-fiókot, az Active Directory-bérlőt, az Azure-előfizetést és a célzott Azure-környezetet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="95c62-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="95c62-110">Az Azure Resource Manager-parancsmagok ezeket a beállításokat használják alapértelmezés szerint az Azure Resource Manager-kérések igénylésekor.</span><span class="sxs-lookup"><span data-stu-id="95c62-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="95c62-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="95c62-111">EXAMPLES</span></span>

### <span data-ttu-id="95c62-112">1. példa: Az aktuális környezet bekérte</span><span class="sxs-lookup"><span data-stu-id="95c62-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="95c62-113">Ebben a példában egy Azure-előfizetéssel jelentkezünk be a fiókunkba a Connect-AzAccount segítségével, majd a Get-AzContext hívja fel az aktuális munkamenet kontextusát.</span><span class="sxs-lookup"><span data-stu-id="95c62-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="95c62-114">2. példa: Az összes rendelkezésre álló környezet felsorolása</span><span class="sxs-lookup"><span data-stu-id="95c62-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="95c62-115">Ebben a példában az összes jelenleg rendelkezésre álló környezet látható.</span><span class="sxs-lookup"><span data-stu-id="95c62-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="95c62-116">A felhasználó a Select-AzContext segítségével választhatja ki a környezetek valamelyikét.</span><span class="sxs-lookup"><span data-stu-id="95c62-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="95c62-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95c62-117">PARAMETERS</span></span>

### <span data-ttu-id="95c62-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c62-118">-DefaultProfile</span></span>
<span data-ttu-id="95c62-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="95c62-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95c62-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="95c62-120">-ListAvailable</span></span>
<span data-ttu-id="95c62-121">List all available contexts in the current session.</span><span class="sxs-lookup"><span data-stu-id="95c62-121">List all available contexts in the current session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c62-122">-Name</span><span class="sxs-lookup"><span data-stu-id="95c62-122">-Name</span></span>
<span data-ttu-id="95c62-123">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="95c62-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c62-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c62-124">CommonParameters</span></span>
<span data-ttu-id="95c62-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95c62-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c62-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95c62-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c62-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95c62-127">INPUTS</span></span>

### <span data-ttu-id="95c62-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="95c62-128">None</span></span>

## <span data-ttu-id="95c62-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95c62-129">OUTPUTS</span></span>

### <span data-ttu-id="95c62-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="95c62-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="95c62-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="95c62-131">NOTES</span></span>

## <span data-ttu-id="95c62-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95c62-132">RELATED LINKS</span></span>

[<span data-ttu-id="95c62-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="95c62-133">Set-AzContext</span></span>](./Set-AzContext.md)

