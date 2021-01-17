---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 193a1dab5bd08489740d0d95f65c6aad1ea85e43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479165"
---
# <span data-ttu-id="83daf-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="83daf-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="83daf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83daf-102">SYNOPSIS</span></span>
<span data-ttu-id="83daf-103">A környezet automatikus mentésének funkciójának metaadatainak megjelenítése, beleértve a környezet automatikus mentésének és a mentett környezet és hitelesítő adatok helyének megjelenítését.</span><span class="sxs-lookup"><span data-stu-id="83daf-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="83daf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="83daf-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83daf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="83daf-105">DESCRIPTION</span></span>
<span data-ttu-id="83daf-106">A környezet automatikus mentésének funkciójának metaadatainak megjelenítése, beleértve a környezet automatikus mentésének és a mentett környezet és hitelesítő adatok helyének megjelenítését.</span><span class="sxs-lookup"><span data-stu-id="83daf-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="83daf-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="83daf-107">EXAMPLES</span></span>

### <span data-ttu-id="83daf-108">Az aktuális munkamenet környezetfüggő mentésének metaadatainak lekérte</span><span class="sxs-lookup"><span data-stu-id="83daf-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="83daf-109">Részletes információk a környezet mentésének helyének és helyének a mentésről.</span><span class="sxs-lookup"><span data-stu-id="83daf-109">Get details about whether and where the context is saved.</span></span>  <span data-ttu-id="83daf-110">A fenti példában az Automatikus mentés funkció le lett tiltva.</span><span class="sxs-lookup"><span data-stu-id="83daf-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="83daf-111">Az aktuális felhasználó környezetfüggő mentésének metaadatainak lekérte</span><span class="sxs-lookup"><span data-stu-id="83daf-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="83daf-112">Részleteket olvashat arról, hogy az aktuális felhasználó környezete alapértelmezés szerint mentve van-e, és hol.</span><span class="sxs-lookup"><span data-stu-id="83daf-112">Get details about whether and where the context is saved by default for the current user.</span></span>  <span data-ttu-id="83daf-113">Vegye figyelembe, hogy ez eltérhet az aktuális munkamenetben aktív beállításoktól.</span><span class="sxs-lookup"><span data-stu-id="83daf-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="83daf-114">A fenti példában az Automatikus mentés funkció engedélyezve van, az adatok pedig az alapértelmezett helyre vannak mentve.</span><span class="sxs-lookup"><span data-stu-id="83daf-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="83daf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83daf-115">PARAMETERS</span></span>

### <span data-ttu-id="83daf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83daf-116">-DefaultProfile</span></span>
<span data-ttu-id="83daf-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="83daf-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83daf-118">-Scope</span><span class="sxs-lookup"><span data-stu-id="83daf-118">-Scope</span></span>
<span data-ttu-id="83daf-119">Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.</span><span class="sxs-lookup"><span data-stu-id="83daf-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="83daf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83daf-120">CommonParameters</span></span>
<span data-ttu-id="83daf-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83daf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83daf-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83daf-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83daf-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83daf-123">INPUTS</span></span>

### <span data-ttu-id="83daf-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="83daf-124">None</span></span>

## <span data-ttu-id="83daf-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83daf-125">OUTPUTS</span></span>

### <span data-ttu-id="83daf-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="83daf-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="83daf-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="83daf-127">NOTES</span></span>

## <span data-ttu-id="83daf-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83daf-128">RELATED LINKS</span></span>
