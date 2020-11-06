---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
ms.openlocfilehash: d0d6c69bb85fcdf851f0f134bb376252525aec91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500480"
---
# <span data-ttu-id="0ac50-101">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="0ac50-101">Get-AzureRmContextAutosaveSetting</span></span>

## <span data-ttu-id="0ac50-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ac50-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac50-103">Metaadatok megjelenítése a környezet automatikus mentés szolgáltatásáról, benne az whterh, ahol a környezet automatikusan Nagyfejeo, valamint a mentett környezet-és hitelesítőadat-adatok is megtalálhatók.</span><span class="sxs-lookup"><span data-stu-id="0ac50-103">Display metadata about the context autosave feature, including whterh the context is automaticallys aved, and where saved context and credential information cna be found.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ac50-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ac50-104">SYNTAX</span></span>

```
Get-AzureRmContextAutosaveSetting [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ac50-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ac50-105">DESCRIPTION</span></span>
<span data-ttu-id="0ac50-106">Metaadatok megjelenítése a környezeti mentés funkcióról, például hogy a környezet automatikusan mentve van-e, illetve hogy hol találhatók a mentett környezet-és hitelesítőadat-adatok.</span><span class="sxs-lookup"><span data-stu-id="0ac50-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="0ac50-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0ac50-107">EXAMPLES</span></span>

### <span data-ttu-id="0ac50-108">A környezet mentése metaadatait az aktuális munkamenethez</span><span class="sxs-lookup"><span data-stu-id="0ac50-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="0ac50-109">Információ arról, hogy a környezet mentése és wehere van-e mentve.</span><span class="sxs-lookup"><span data-stu-id="0ac50-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="0ac50-110">A fenti példában az automatikus mentés funkció le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="0ac50-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="0ac50-111">A környezet mentése metaadatait az aktuális felhasználó számára</span><span class="sxs-lookup"><span data-stu-id="0ac50-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="0ac50-112">Itt részletesen megtudhatja, hogy az aktuális felhasználó alapértelmezés szerint menti-e a környezetet és a wehere.</span><span class="sxs-lookup"><span data-stu-id="0ac50-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="0ac50-113">Fontos tudni, hogy ez az aktuális munkamenetben aktív beállításoktól eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="0ac50-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="0ac50-114">A fenti példában engedélyezte az automatikus mentés funkciót, és az adatot az alapértelmezett helyre menti.</span><span class="sxs-lookup"><span data-stu-id="0ac50-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="0ac50-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ac50-115">PARAMETERS</span></span>

### <span data-ttu-id="0ac50-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac50-116">-DefaultProfile</span></span>
<span data-ttu-id="0ac50-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0ac50-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ac50-118">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="0ac50-118">-Scope</span></span>
<span data-ttu-id="0ac50-119">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="0ac50-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="0ac50-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac50-120">CommonParameters</span></span>
<span data-ttu-id="0ac50-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ac50-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac50-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ac50-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac50-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ac50-123">INPUTS</span></span>

### <span data-ttu-id="0ac50-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="0ac50-124">None</span></span>

## <span data-ttu-id="0ac50-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ac50-125">OUTPUTS</span></span>

### <span data-ttu-id="0ac50-126">Microsoft. Azure. commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="0ac50-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="0ac50-127">A jelenlegi automatikus mentés beállításairól szóló információk, például hogy engedélyezve van-e az automatikus mentés az aktuális felhasználó számára, és hogy hol vannak mentve a környezet és a hitelesítőadat-fájlok.</span><span class="sxs-lookup"><span data-stu-id="0ac50-127">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="0ac50-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ac50-128">NOTES</span></span>

## <span data-ttu-id="0ac50-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ac50-129">RELATED LINKS</span></span>

