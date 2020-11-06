---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: 85c3791e9947ce6f7ad2ce365239da16cec17b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504012"
---
# <span data-ttu-id="ba545-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="ba545-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="ba545-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba545-102">SYNOPSIS</span></span>
<span data-ttu-id="ba545-103">Kapcsolja ki az automatikus mentés Azure hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="ba545-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="ba545-104">A rendszer a PowerShell-ablak legközelebbi megnyitásakor elfelejti a bejelentkezési adatait</span><span class="sxs-lookup"><span data-stu-id="ba545-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba545-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba545-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba545-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba545-106">DESCRIPTION</span></span>
<span data-ttu-id="ba545-107">Kapcsolja ki az automatikus mentés Azure hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="ba545-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="ba545-108">A rendszer a PowerShell-ablak legközelebbi megnyitásakor elfelejti a bejelentkezési adatait</span><span class="sxs-lookup"><span data-stu-id="ba545-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="ba545-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ba545-109">EXAMPLES</span></span>

### <span data-ttu-id="ba545-110">A környezet automatikus mentésének letiltása</span><span class="sxs-lookup"><span data-stu-id="ba545-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="ba545-111">Tiltsa le az automatikus mentés funkciót az aktuális felhasználónál.</span><span class="sxs-lookup"><span data-stu-id="ba545-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="ba545-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba545-112">PARAMETERS</span></span>

### <span data-ttu-id="ba545-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba545-113">-DefaultProfile</span></span>
<span data-ttu-id="ba545-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ba545-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba545-115">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="ba545-115">-Scope</span></span>
<span data-ttu-id="ba545-116">A környezeti változások hatókörét határozza meg, például a wheher módosítása csak a cusrrent folyamatra, illetve a felhasználó által indított összes munkamenetre érvényes.</span><span class="sxs-lookup"><span data-stu-id="ba545-116">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="ba545-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba545-117">-Confirm</span></span>
<span data-ttu-id="ba545-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba545-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba545-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba545-119">-WhatIf</span></span>
<span data-ttu-id="ba545-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba545-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba545-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba545-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba545-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba545-122">CommonParameters</span></span>
<span data-ttu-id="ba545-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba545-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba545-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba545-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba545-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba545-125">INPUTS</span></span>

### <span data-ttu-id="ba545-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="ba545-126">None</span></span>

## <span data-ttu-id="ba545-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba545-127">OUTPUTS</span></span>

### <span data-ttu-id="ba545-128">Microsoft. Azure. commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="ba545-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="ba545-129">A jelenlegi automatikus mentés beállításairól szóló információk, például hogy engedélyezve van-e az automatikus mentés az aktuális felhasználó számára, és hogy hol vannak mentve a környezet és a hitelesítőadat-fájlok.</span><span class="sxs-lookup"><span data-stu-id="ba545-129">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="ba545-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba545-130">NOTES</span></span>

## <span data-ttu-id="ba545-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba545-131">RELATED LINKS</span></span>

