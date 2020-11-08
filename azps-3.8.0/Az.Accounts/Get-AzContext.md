---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: dab6388205c00ee457b7f8095f0f529f591b304f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013022"
---
# <span data-ttu-id="b426b-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="b426b-101">Get-AzContext</span></span>

## <span data-ttu-id="b426b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b426b-102">SYNOPSIS</span></span>
<span data-ttu-id="b426b-103">Az Azure Resource Manager-kérések hitelesítéséhez használt metaadatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b426b-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="b426b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b426b-104">SYNTAX</span></span>

### <span data-ttu-id="b426b-105">GetSingleContext (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b426b-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="b426b-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="b426b-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b426b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b426b-107">DESCRIPTION</span></span>
<span data-ttu-id="b426b-108">A Get-AzContext parancsmag az Azure Resource Manager-kérések hitelesítéséhez használt jelenlegi metaadatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b426b-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="b426b-109">Ez a parancsmag az Active Directory-fiókot, az Active Directory-bérlőt, az Azure-előfizetést és a célzott Azure-környezetet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b426b-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="b426b-110">Az Azure Resource Manager-parancsmagok alapértelmezés szerint ezeket a beállításokat használják az Azure Resource Manager-kérések készítésekor.</span><span class="sxs-lookup"><span data-stu-id="b426b-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="b426b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b426b-111">EXAMPLES</span></span>

### <span data-ttu-id="b426b-112">Példa 1: a jelenlegi környezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="b426b-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="b426b-113">Ebben a példában egy Azure-előfizetéssel jelentkezik be a fiókba a Connect-AzAccount, és az aktuális munkamenet kontextusát a Get-AzContext hívásával fogjuk használni.</span><span class="sxs-lookup"><span data-stu-id="b426b-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="b426b-114">2. példa: az összes elérhető kontextus listázása</span><span class="sxs-lookup"><span data-stu-id="b426b-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="b426b-115">Ebben a példában az összes jelenleg elérhető kontextus megjelenik.</span><span class="sxs-lookup"><span data-stu-id="b426b-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="b426b-116">A felhasználó a Select-AzContext kiválaszthatja az alábbi környezetek egyikét.</span><span class="sxs-lookup"><span data-stu-id="b426b-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="b426b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b426b-117">PARAMETERS</span></span>

### <span data-ttu-id="b426b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b426b-118">-DefaultProfile</span></span>
<span data-ttu-id="b426b-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b426b-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b426b-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="b426b-120">-ListAvailable</span></span>
<span data-ttu-id="b426b-121">Az összes elérhető környezet listázása az aktuális munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="b426b-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="b426b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b426b-122">-Name</span></span>
<span data-ttu-id="b426b-123">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="b426b-123">The name of the context</span></span>

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

### <span data-ttu-id="b426b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b426b-124">CommonParameters</span></span>
<span data-ttu-id="b426b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b426b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b426b-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b426b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b426b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b426b-127">INPUTS</span></span>

### <span data-ttu-id="b426b-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="b426b-128">None</span></span>

## <span data-ttu-id="b426b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b426b-129">OUTPUTS</span></span>

### <span data-ttu-id="b426b-130">Microsoft. Azure. Command. profil. models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="b426b-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="b426b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b426b-131">NOTES</span></span>

## <span data-ttu-id="b426b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b426b-132">RELATED LINKS</span></span>

[<span data-ttu-id="b426b-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="b426b-133">Set-AzContext</span></span>](./Set-AzContext.md)

