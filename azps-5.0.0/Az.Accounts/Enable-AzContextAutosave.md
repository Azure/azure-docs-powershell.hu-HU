---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193976"
---
# <span data-ttu-id="5e77f-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="5e77f-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="5e77f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e77f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e77f-103">Az Azure-környezetek az aktív előfizetést jelképező PowerShell-objektumok, valamint az Azure Cloud-hoz való csatlakozáshoz szükséges hitelesítési adatok.</span><span class="sxs-lookup"><span data-stu-id="5e77f-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="5e77f-104">Az Azure-környezetek használatakor az Azure PowerShell-nek nem kell minden alkalommal újra hitelesítenie a fiókját az előfizetések váltása során.</span><span class="sxs-lookup"><span data-stu-id="5e77f-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="5e77f-105">További tudnivalókat az [Azure PowerShell környezet-objektumai](https://docs.microsoft.com/powershell/azure/context-persistence)című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="5e77f-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="5e77f-106">Ez a parancsmag lehetővé teszi az Azure-környezet adatainak mentését és automatikus betöltését PowerShell-folyamat indításakor.</span><span class="sxs-lookup"><span data-stu-id="5e77f-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="5e77f-107">Új ablak megnyitásakor például</span><span class="sxs-lookup"><span data-stu-id="5e77f-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="5e77f-108">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e77f-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e77f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e77f-109">DESCRIPTION</span></span>

<span data-ttu-id="5e77f-110">Lehetővé teszi az Azure-környezet adatainak mentését és automatikus betöltését a PowerShell-folyamat indításakor.</span><span class="sxs-lookup"><span data-stu-id="5e77f-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="5e77f-111">A környezet a környezetet érintő bármely parancsmag végrehajtásának végén tárolódik.</span><span class="sxs-lookup"><span data-stu-id="5e77f-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="5e77f-112">Például bármely profil parancsmag.</span><span class="sxs-lookup"><span data-stu-id="5e77f-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="5e77f-113">Ha a felhasználó hitelesítését használja, a tokenek bármelyik parancsmag futtatása során frissíthetők.</span><span class="sxs-lookup"><span data-stu-id="5e77f-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="5e77f-114">Példák</span><span class="sxs-lookup"><span data-stu-id="5e77f-114">EXAMPLES</span></span>

### <span data-ttu-id="5e77f-115">Példa 1: az aktuális felhasználó automatikus mentési hitelesítő adatainak engedélyezése</span><span class="sxs-lookup"><span data-stu-id="5e77f-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="5e77f-116">A hitelesítő adatok automatikus mentésének bekapcsolása az aktuális felhasználónál</span><span class="sxs-lookup"><span data-stu-id="5e77f-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="5e77f-117">Minden alkalommal, amikor egy PowerShell-ablak van megnyitva, a jelenlegi környezete bejelentkezés nélkül emlékezetbe kerül.</span><span class="sxs-lookup"><span data-stu-id="5e77f-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="5e77f-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="5e77f-118">Example 2</span></span>

<span data-ttu-id="5e77f-119">Engedélyezze az Azure hitelesítő adatait, fiókját és előfizetési adatait, hogy a PowerShell-munkamenet PowerShell-ablakának megnyitásakor a program mentse és automatikusan betöltse a fájlt.</span><span class="sxs-lookup"><span data-stu-id="5e77f-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="5e77f-120">autogenerated</span><span class="sxs-lookup"><span data-stu-id="5e77f-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="5e77f-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e77f-121">PARAMETERS</span></span>

### <span data-ttu-id="5e77f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e77f-122">-DefaultProfile</span></span>

<span data-ttu-id="5e77f-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5e77f-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="5e77f-124">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="5e77f-124">-Scope</span></span>

<span data-ttu-id="5e77f-125">A környezeti változások hatókörét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5e77f-125">Determines the scope of context changes.</span></span> <span data-ttu-id="5e77f-126">Például a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.</span><span class="sxs-lookup"><span data-stu-id="5e77f-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="5e77f-127">A hatókör módosításai a `CurrentUser` felhasználó által indított összes PowerShell-munkamenetre érvényesek lesznek.</span><span class="sxs-lookup"><span data-stu-id="5e77f-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="5e77f-128">Ha egy adott munkamenetnek eltérő beállításokat kell használnia, használja a hatókört `Process` .</span><span class="sxs-lookup"><span data-stu-id="5e77f-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e77f-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5e77f-129">-Confirm</span></span>

<span data-ttu-id="5e77f-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5e77f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e77f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e77f-131">-WhatIf</span></span>

<span data-ttu-id="5e77f-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5e77f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e77f-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e77f-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="5e77f-134">Gyakori paraméterek</span><span class="sxs-lookup"><span data-stu-id="5e77f-134">Common Parameters</span></span>

<span data-ttu-id="5e77f-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e77f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e77f-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5e77f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e77f-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e77f-137">INPUTS</span></span>

### <span data-ttu-id="5e77f-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="5e77f-138">None</span></span>

## <span data-ttu-id="5e77f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e77f-139">OUTPUTS</span></span>

### <span data-ttu-id="5e77f-140">Microsoft. Azure. commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="5e77f-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="5e77f-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e77f-141">NOTES</span></span>

## <span data-ttu-id="5e77f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e77f-142">RELATED LINKS</span></span>
