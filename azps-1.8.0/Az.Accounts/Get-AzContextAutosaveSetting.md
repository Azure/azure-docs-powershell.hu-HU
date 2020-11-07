---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: a6361fabaa05d99b35874ce0de388ed0fc1bdfa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665801"
---
# <span data-ttu-id="79423-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="79423-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="79423-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79423-102">SYNOPSIS</span></span>
<span data-ttu-id="79423-103">Metaadatok megjelenítése a környezeti mentés funkcióról, például hogy a környezet automatikusan mentve van-e, illetve hogy hol találhatók a mentett környezet-és hitelesítőadat-adatok.</span><span class="sxs-lookup"><span data-stu-id="79423-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="79423-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79423-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79423-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="79423-105">DESCRIPTION</span></span>
<span data-ttu-id="79423-106">Metaadatok megjelenítése a környezeti mentés funkcióról, például hogy a környezet automatikusan mentve van-e, illetve hogy hol találhatók a mentett környezet-és hitelesítőadat-adatok.</span><span class="sxs-lookup"><span data-stu-id="79423-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="79423-107">Példák</span><span class="sxs-lookup"><span data-stu-id="79423-107">EXAMPLES</span></span>

### <span data-ttu-id="79423-108">A környezet mentése metaadatait az aktuális munkamenethez</span><span class="sxs-lookup"><span data-stu-id="79423-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="79423-109">Információ arról, hogy a környezet mentése és wehere van-e mentve.</span><span class="sxs-lookup"><span data-stu-id="79423-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="79423-110">A fenti példában az automatikus mentés funkció le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="79423-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="79423-111">A környezet mentése metaadatait az aktuális felhasználó számára</span><span class="sxs-lookup"><span data-stu-id="79423-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="79423-112">Itt részletesen megtudhatja, hogy az aktuális felhasználó alapértelmezés szerint menti-e a környezetet és a wehere.</span><span class="sxs-lookup"><span data-stu-id="79423-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="79423-113">Fontos tudni, hogy ez az aktuális munkamenetben aktív beállításoktól eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="79423-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="79423-114">A fenti példában engedélyezte az automatikus mentés funkciót, és az adatot az alapértelmezett helyre menti.</span><span class="sxs-lookup"><span data-stu-id="79423-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="79423-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79423-115">PARAMETERS</span></span>

### <span data-ttu-id="79423-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79423-116">-DefaultProfile</span></span>
<span data-ttu-id="79423-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="79423-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79423-118">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="79423-118">-Scope</span></span>
<span data-ttu-id="79423-119">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="79423-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="79423-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79423-120">CommonParameters</span></span>
<span data-ttu-id="79423-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79423-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79423-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79423-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79423-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79423-123">INPUTS</span></span>

### <span data-ttu-id="79423-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="79423-124">None</span></span>

## <span data-ttu-id="79423-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79423-125">OUTPUTS</span></span>

### <span data-ttu-id="79423-126">Microsoft. Azure. commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="79423-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="79423-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79423-127">NOTES</span></span>

## <span data-ttu-id="79423-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79423-128">RELATED LINKS</span></span>
