---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/import-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
ms.openlocfilehash: b78095ef55fa647cc11ea3e2d2b1a49089407747
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502528"
---
# <span data-ttu-id="3a9ab-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="3a9ab-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="3a9ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a9ab-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9ab-103">Azure-hitelesítési adatok betöltése egy fájlból.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-103">Loads Azure authentication information from a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a9ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a9ab-104">SYNTAX</span></span>

### <span data-ttu-id="3a9ab-105">ProfileFromDisk (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3a9ab-105">ProfileFromDisk (Default)</span></span>
```
Import-AzureRmContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a9ab-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="3a9ab-106">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a9ab-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a9ab-107">DESCRIPTION</span></span>
<span data-ttu-id="3a9ab-108">A Import-AzureRmContext parancsmag az Azure-környezet és-környezet beállításához betölti a fájlok hitelesítési adatait.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="3a9ab-109">Az aktuális munkamenetben futtatott parancsmagok ezekkel az információkkal hitelesíthetők az Azure Resource Manager kérései között.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="3a9ab-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3a9ab-110">EXAMPLES</span></span>

### <span data-ttu-id="3a9ab-111">1. példa: környezet importálása AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="3a9ab-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Connect-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="3a9ab-112">Ebben a példában egy olyan környezetet importál egy PSAzureProfile, amely át lett adva a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="3a9ab-113">2. példa: környezet importálása JSON-fájlból</span><span class="sxs-lookup"><span data-stu-id="3a9ab-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="3a9ab-114">Ebben a példában egy JSON-fájl egy olyan környezetét jelöli ki, amely át lett adva a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="3a9ab-115">Ezt a JSON-fájlt a Save-AzureRmContext hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-115">This JSON file can be created from Save-AzureRmContext.</span></span>

## <span data-ttu-id="3a9ab-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a9ab-116">PARAMETERS</span></span>

### <span data-ttu-id="3a9ab-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="3a9ab-117">-AzureContext</span></span>
<span data-ttu-id="3a9ab-118">Azt az Azure-környezetet adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-118">Specifies the Azure context from which this cmdlet reads.</span></span> <span data-ttu-id="3a9ab-119">Ha nem ad meg környezetet, a parancsmag a helyi alapértelmezett környezetből olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a9ab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9ab-120">-DefaultProfile</span></span>
<span data-ttu-id="3a9ab-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3a9ab-121">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a9ab-122">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="3a9ab-122">-Path</span></span>
<span data-ttu-id="3a9ab-123">A Save-AzureRMContext paranccsal mentett környezeti információk elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-123">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a9ab-124">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="3a9ab-124">-Scope</span></span>
<span data-ttu-id="3a9ab-125">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-125">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9ab-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3a9ab-126">-Confirm</span></span>
<span data-ttu-id="3a9ab-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9ab-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a9ab-128">-WhatIf</span></span>
<span data-ttu-id="3a9ab-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a9ab-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9ab-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9ab-131">CommonParameters</span></span>
<span data-ttu-id="3a9ab-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a9ab-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9ab-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a9ab-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9ab-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a9ab-134">INPUTS</span></span>

### <span data-ttu-id="3a9ab-135">Microsoft. Azure. commands. Common. Authentication. models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="3a9ab-135">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="3a9ab-136">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiókok és előfizetések halmazát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-136">Contains the set of credentials, accounts, and subscriptions that are used to communicate with Azure.</span></span>

## <span data-ttu-id="3a9ab-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a9ab-137">OUTPUTS</span></span>

### <span data-ttu-id="3a9ab-138">Microsoft. Azure. Command. profil. models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="3a9ab-138">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>
<span data-ttu-id="3a9ab-139">Azokat a hitelesítő adatokat, fiókokat és előfizetéseket tartalmazza, amelyekkel kommunikálni tud az Azuretal.</span><span class="sxs-lookup"><span data-stu-id="3a9ab-139">Contains the set of credentials, accounts, and subscriptions that can be used to communicate with Azure.</span></span>

## <span data-ttu-id="3a9ab-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a9ab-140">NOTES</span></span>

## <span data-ttu-id="3a9ab-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a9ab-141">RELATED LINKS</span></span>

