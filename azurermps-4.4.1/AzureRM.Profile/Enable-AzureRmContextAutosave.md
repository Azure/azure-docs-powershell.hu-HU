---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
ms.openlocfilehash: d785cd364cd67a9d79f8710ef664048b8f54b8ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496975"
---
# <span data-ttu-id="e90e8-101">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="e90e8-101">Enable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="e90e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e90e8-102">SYNOPSIS</span></span>
<span data-ttu-id="e90e8-103">A PowerShell-ablak megnyitásakor az Azure-hitelesítő adatok, a fiók és az előfizetési adatok menthetők és automatikusan betölthetők.</span><span class="sxs-lookup"><span data-stu-id="e90e8-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e90e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e90e8-104">SYNTAX</span></span>

```
Enable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e90e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e90e8-105">DESCRIPTION</span></span>
<span data-ttu-id="e90e8-106">A PowerShell-ablak megnyitásakor az Azure-hitelesítő adatok, a fiók és az előfizetési adatok menthetők és automatikusan betölthetők.</span><span class="sxs-lookup"><span data-stu-id="e90e8-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="e90e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e90e8-107">EXAMPLES</span></span>

### <span data-ttu-id="e90e8-108">Az aktuális felhasználó automatikus mentésére vonatkozó hitelesítő adatok engedélyezése</span><span class="sxs-lookup"><span data-stu-id="e90e8-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzureRmContextAutosave
```

<span data-ttu-id="e90e8-109">A hitelesítő adatok automatikus mentésének bekapcsolása az aktuális felhasználónál</span><span class="sxs-lookup"><span data-stu-id="e90e8-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="e90e8-110">Minden alkalommal, amikor egy PowerShell-ablak van megnyitva, a jelenlegi környezete bejelentkezés nélkül emlékezni fog.</span><span class="sxs-lookup"><span data-stu-id="e90e8-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="e90e8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e90e8-111">PARAMETERS</span></span>

### <span data-ttu-id="e90e8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e90e8-112">-DefaultProfile</span></span>
<span data-ttu-id="e90e8-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e90e8-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e90e8-114">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="e90e8-114">-Scope</span></span>
<span data-ttu-id="e90e8-115">A környezeti változások hatókörét határozza meg, például a wheher módosítása csak a cusrrent folyamatra, illetve a felhasználó által indított összes munkamenetre érvényes.</span><span class="sxs-lookup"><span data-stu-id="e90e8-115">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="e90e8-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e90e8-116">-Confirm</span></span>
<span data-ttu-id="e90e8-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e90e8-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e90e8-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e90e8-118">-WhatIf</span></span>
<span data-ttu-id="e90e8-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e90e8-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e90e8-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e90e8-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e90e8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e90e8-121">CommonParameters</span></span>
<span data-ttu-id="e90e8-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e90e8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e90e8-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e90e8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e90e8-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e90e8-124">INPUTS</span></span>

### <span data-ttu-id="e90e8-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="e90e8-125">None</span></span>

## <span data-ttu-id="e90e8-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e90e8-126">OUTPUTS</span></span>

### <span data-ttu-id="e90e8-127">Microsoft. Azure. commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="e90e8-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="e90e8-128">A jelenlegi automatikus mentés beállításairól szóló információk, például hogy engedélyezve van-e az automatikus mentés az aktuális felhasználó számára, és hogy hol vannak mentve a környezet és a hitelesítőadat-fájlok.</span><span class="sxs-lookup"><span data-stu-id="e90e8-128">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="e90e8-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e90e8-129">NOTES</span></span>

## <span data-ttu-id="e90e8-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e90e8-130">RELATED LINKS</span></span>

