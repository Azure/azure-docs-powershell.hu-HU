---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/import-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
ms.openlocfilehash: 590557d883979ac3f23decd88695695df9aecc0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495784"
---
# <span data-ttu-id="09551-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="09551-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="09551-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09551-102">SYNOPSIS</span></span>
<span data-ttu-id="09551-103">Azure-hitelesítési adatok betöltése egy fájlból.</span><span class="sxs-lookup"><span data-stu-id="09551-103">Loads Azure authentication information from a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09551-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09551-104">SYNTAX</span></span>

### <span data-ttu-id="09551-105">ProfileFromDisk (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09551-105">ProfileFromDisk (Default)</span></span>
```
Import-AzureRmContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09551-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="09551-106">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09551-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="09551-107">DESCRIPTION</span></span>
<span data-ttu-id="09551-108">A Import-AzureRmContext parancsmag az Azure-környezet és-környezet beállításához betölti a fájlok hitelesítési adatait.</span><span class="sxs-lookup"><span data-stu-id="09551-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="09551-109">Az aktuális munkamenetben futtatott parancsmagok ezekkel az információkkal hitelesíthetők az Azure Resource Manager kérései között.</span><span class="sxs-lookup"><span data-stu-id="09551-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="09551-110">Példák</span><span class="sxs-lookup"><span data-stu-id="09551-110">EXAMPLES</span></span>

### <span data-ttu-id="09551-111">1. példa: környezet importálása AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="09551-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Connect-AzureRmAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="09551-112">Ebben a példában egy olyan környezetet importál egy PSAzureProfile, amely át lett adva a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="09551-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="09551-113">2. példa: környezet importálása JSON-fájlból</span><span class="sxs-lookup"><span data-stu-id="09551-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="09551-114">Ebben a példában egy JSON-fájl egy olyan környezetét jelöli ki, amely át lett adva a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="09551-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="09551-115">Ezt a JSON-fájlt a Save-AzureRmContext hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="09551-115">This JSON file can be created from Save-AzureRmContext.</span></span>

## <span data-ttu-id="09551-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09551-116">PARAMETERS</span></span>

### <span data-ttu-id="09551-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="09551-117">-AzureContext</span></span>
<span data-ttu-id="09551-118">Azt az Azure-környezetet adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="09551-118">Specifies the Azure context from which this cmdlet reads.</span></span> <span data-ttu-id="09551-119">Ha nem ad meg környezetet, a parancsmag a helyi alapértelmezett környezetből olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="09551-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09551-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09551-120">-DefaultProfile</span></span>
<span data-ttu-id="09551-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="09551-121">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09551-122">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="09551-122">-Path</span></span>
<span data-ttu-id="09551-123">A Save-AzureRMContext paranccsal mentett környezeti információk elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="09551-123">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: System.String
Parameter Sets: ProfileFromDisk
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09551-124">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="09551-124">-Scope</span></span>
<span data-ttu-id="09551-125">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="09551-125">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09551-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="09551-126">-Confirm</span></span>
<span data-ttu-id="09551-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="09551-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09551-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09551-128">-WhatIf</span></span>
<span data-ttu-id="09551-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="09551-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09551-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09551-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09551-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09551-131">CommonParameters</span></span>
<span data-ttu-id="09551-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09551-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09551-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09551-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09551-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09551-134">INPUTS</span></span>

### <span data-ttu-id="09551-135">Microsoft. Azure. commands. Common. Authentication. models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="09551-135">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="09551-136">System. String</span><span class="sxs-lookup"><span data-stu-id="09551-136">System.String</span></span>

## <span data-ttu-id="09551-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09551-137">OUTPUTS</span></span>

### <span data-ttu-id="09551-138">Microsoft. Azure. Command. profil. models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="09551-138">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="09551-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09551-139">NOTES</span></span>

## <span data-ttu-id="09551-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09551-140">RELATED LINKS</span></span>
