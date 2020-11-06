---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: 96b9b5a6bec10082d7b004dcede73b743a7e538b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502536"
---
# <span data-ttu-id="3eb85-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="3eb85-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="3eb85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3eb85-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb85-103">Az Azure Resource Manager-kérések hitelesítéséhez használt metaadatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3eb85-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eb85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3eb85-104">SYNTAX</span></span>

### <span data-ttu-id="3eb85-105">GetSingleContext (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3eb85-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="3eb85-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="3eb85-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3eb85-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3eb85-107">DESCRIPTION</span></span>
<span data-ttu-id="3eb85-108">A Get-AzureRmContext parancsmag az Azure Resource Manager-kérések hitelesítéséhez használt jelenlegi metaadatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3eb85-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="3eb85-109">Ez a parancsmag az Active Directory-fiókot, az Active Directory-bérlőt, az Azure-előfizetést és a célzott Azure-környezetet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3eb85-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="3eb85-110">Az Azure Resource Manager-parancsmagok alapértelmezés szerint ezeket a beállításokat használják az Azure Resource Manager-kérések készítésekor.</span><span class="sxs-lookup"><span data-stu-id="3eb85-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="3eb85-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3eb85-111">EXAMPLES</span></span>

### <span data-ttu-id="3eb85-112">Példa 1: a jelenlegi környezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="3eb85-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="3eb85-113">Ebben a példában egy Azure-előfizetéssel jelentkezik be a fiókba a Connect-AzureRmAccount, és az aktuális munkamenet kontextusát a Get-AzureRmContext hívásával fogjuk használni.</span><span class="sxs-lookup"><span data-stu-id="3eb85-113">In this example we are logging into our account with an Azure subscription using Connect-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="3eb85-114">2. példa: az összes elérhető kontextus listázása</span><span class="sxs-lookup"><span data-stu-id="3eb85-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                  : Test
Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :

Name                  : Production
Environment           : AzureCloud
Account               : prod@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Production Subscription
CurrentStorageAccount :
```

<span data-ttu-id="3eb85-115">Ebben a példában az összes jelenleg elérhető kontextus megjelenik.</span><span class="sxs-lookup"><span data-stu-id="3eb85-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="3eb85-116">A felhasználó a Select-AzureRmContext kiválaszthatja az alábbi környezetek egyikét.</span><span class="sxs-lookup"><span data-stu-id="3eb85-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="3eb85-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3eb85-117">PARAMETERS</span></span>

### <span data-ttu-id="3eb85-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb85-118">-DefaultProfile</span></span>
<span data-ttu-id="3eb85-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3eb85-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb85-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="3eb85-120">-ListAvailable</span></span>
<span data-ttu-id="3eb85-121">Az összes elérhető környezet listázása az aktuális munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="3eb85-121">List all available contexts in the current session.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllContexts
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb85-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3eb85-122">-Name</span></span>
<span data-ttu-id="3eb85-123">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="3eb85-123">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: GetSingleContext
Aliases: 
Accepted values: Default

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb85-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb85-124">CommonParameters</span></span>
<span data-ttu-id="3eb85-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3eb85-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb85-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb85-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb85-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3eb85-127">INPUTS</span></span>

### <span data-ttu-id="3eb85-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="3eb85-128">None</span></span>
<span data-ttu-id="3eb85-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3eb85-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3eb85-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3eb85-130">OUTPUTS</span></span>

### <span data-ttu-id="3eb85-131">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="3eb85-131">PSAzureContext</span></span>
<span data-ttu-id="3eb85-132">Ez a parancsmag az Azure Resource Manager-parancsmagok által használt fiókot, bérlőt és előfizetést számítja ki.</span><span class="sxs-lookup"><span data-stu-id="3eb85-132">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="3eb85-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3eb85-133">NOTES</span></span>

## <span data-ttu-id="3eb85-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3eb85-134">RELATED LINKS</span></span>

[<span data-ttu-id="3eb85-135">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="3eb85-135">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

