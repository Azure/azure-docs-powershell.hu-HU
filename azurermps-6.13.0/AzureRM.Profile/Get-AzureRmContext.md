---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: dbe93ca98fe8cf7a0a22f2b52a17a17e7222c261
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493619"
---
# <span data-ttu-id="e3719-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e3719-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="e3719-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3719-102">SYNOPSIS</span></span>
<span data-ttu-id="e3719-103">Az Azure Resource Manager-kérések hitelesítéséhez használt metaadatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e3719-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3719-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3719-104">SYNTAX</span></span>

### <span data-ttu-id="e3719-105">GetSingleContext (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3719-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="e3719-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="e3719-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3719-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3719-107">DESCRIPTION</span></span>
<span data-ttu-id="e3719-108">A Get-AzureRmContext parancsmag az Azure Resource Manager-kérések hitelesítéséhez használt jelenlegi metaadatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e3719-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="e3719-109">Ez a parancsmag az Active Directory-fiókot, az Active Directory-bérlőt, az Azure-előfizetést és a célzott Azure-környezetet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e3719-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="e3719-110">Az Azure Resource Manager-parancsmagok alapértelmezés szerint ezeket a beállításokat használják az Azure Resource Manager-kérések készítésekor.</span><span class="sxs-lookup"><span data-stu-id="e3719-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="e3719-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e3719-111">EXAMPLES</span></span>

### <span data-ttu-id="e3719-112">Példa 1: a jelenlegi környezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="e3719-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="e3719-113">Ebben a példában egy Azure-előfizetéssel jelentkezik be a fiókba a Connect-AzureRmAccount, és az aktuális munkamenet kontextusát a Get-AzureRmContext hívásával fogjuk használni.</span><span class="sxs-lookup"><span data-stu-id="e3719-113">In this example we are logging into our account with an Azure subscription using Connect-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="e3719-114">2. példa: az összes elérhető kontextus listázása</span><span class="sxs-lookup"><span data-stu-id="e3719-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="e3719-115">Ebben a példában az összes jelenleg elérhető kontextus megjelenik.</span><span class="sxs-lookup"><span data-stu-id="e3719-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="e3719-116">A felhasználó a Select-AzureRmContext kiválaszthatja az alábbi környezetek egyikét.</span><span class="sxs-lookup"><span data-stu-id="e3719-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="e3719-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3719-117">PARAMETERS</span></span>

### <span data-ttu-id="e3719-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3719-118">-DefaultProfile</span></span>
<span data-ttu-id="e3719-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e3719-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3719-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="e3719-120">-ListAvailable</span></span>
<span data-ttu-id="e3719-121">Az összes elérhető környezet listázása az aktuális munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="e3719-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="e3719-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3719-122">-Name</span></span>
<span data-ttu-id="e3719-123">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="e3719-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:
Accepted values: Default

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3719-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3719-124">CommonParameters</span></span>
<span data-ttu-id="e3719-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3719-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3719-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3719-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3719-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3719-127">INPUTS</span></span>

### <span data-ttu-id="e3719-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="e3719-128">None</span></span>

## <span data-ttu-id="e3719-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3719-129">OUTPUTS</span></span>

### <span data-ttu-id="e3719-130">Microsoft. Azure. Command. profil. models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="e3719-130">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="e3719-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3719-131">NOTES</span></span>

## <span data-ttu-id="e3719-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3719-132">RELATED LINKS</span></span>

[<span data-ttu-id="e3719-133">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="e3719-133">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

