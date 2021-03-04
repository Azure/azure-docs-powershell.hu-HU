---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 8bca1314433f8fcbcc0c9f395783bbb3d9835ffb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943193"
---
# <span data-ttu-id="f2891-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="f2891-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="f2891-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2891-102">SYNOPSIS</span></span>
<span data-ttu-id="f2891-103">Az Azure-környezetek olyan PowerShell-objektumok, amelyek az aktív előfizetést képviselik, amelyeken parancsokat futtathat, valamint az Azure-felhőhöz való csatlakozáshoz szükséges hitelesítési adatok.</span><span class="sxs-lookup"><span data-stu-id="f2891-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="f2891-104">Az Azure-környezetek esetén az Azure PowerShellnek nem kell minden alkalommal újra hitelesenie a fiókját, amikor előfizetést vált.</span><span class="sxs-lookup"><span data-stu-id="f2891-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="f2891-105">További információért lásd az [Azure PowerShell környezetobjektumokat.](https://docs.microsoft.com/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="f2891-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="f2891-106">Ez a parancsmag lehetővé teszi az Azure környezetinformációk mentését és automatikus betöltéset a PowerShell-folyamat elindítani.</span><span class="sxs-lookup"><span data-stu-id="f2891-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="f2891-107">Új ablak megnyitásakor például.</span><span class="sxs-lookup"><span data-stu-id="f2891-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="f2891-108">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2891-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2891-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2891-109">DESCRIPTION</span></span>

<span data-ttu-id="f2891-110">Lehetővé teszi az Azure környezetinformációk mentését és automatikus betöltését a PowerShell-folyamat indításakor.</span><span class="sxs-lookup"><span data-stu-id="f2891-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="f2891-111">A környezet a környezetre befolyásoló parancsmagok végrehajtásának végén lesz mentve.</span><span class="sxs-lookup"><span data-stu-id="f2891-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="f2891-112">Például egy profil-parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f2891-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="f2891-113">Ha felhasználói hitelesítést használ, a parancsmagok futtatása során a jogkivonatok frissíthetők.</span><span class="sxs-lookup"><span data-stu-id="f2891-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="f2891-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2891-114">EXAMPLES</span></span>

### <span data-ttu-id="f2891-115">1. példa: A hitelesítő adatok automatikus mentésének engedélyezése az aktuális felhasználónál</span><span class="sxs-lookup"><span data-stu-id="f2891-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="f2891-116">Kapcsolja be a hitelesítő adatok automatikus mentését az aktuális felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="f2891-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="f2891-117">Amikor megnyit egy PowerShell-ablakot, a rendszer bejelentkezés nélkül emlékezni fog az aktuális környezetre.</span><span class="sxs-lookup"><span data-stu-id="f2891-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="f2891-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="f2891-118">Example 2</span></span>

<span data-ttu-id="f2891-119">Az Azure-beli hitelesítő adatok, fiókok és előfizetési adatok mentésének és automatikus betölt használatának engedélyezése, amikor ebben a PowerShell-munkamenetben megnyit egy PowerShell-ablakot.</span><span class="sxs-lookup"><span data-stu-id="f2891-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="f2891-120">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="f2891-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="f2891-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2891-121">PARAMETERS</span></span>

### <span data-ttu-id="f2891-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2891-122">-DefaultProfile</span></span>

<span data-ttu-id="f2891-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f2891-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="f2891-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="f2891-124">-Scope</span></span>

<span data-ttu-id="f2891-125">Meghatározza a környezetváltozások hatókörét.</span><span class="sxs-lookup"><span data-stu-id="f2891-125">Determines the scope of context changes.</span></span> <span data-ttu-id="f2891-126">Például, hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.</span><span class="sxs-lookup"><span data-stu-id="f2891-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="f2891-127">A hatókörrel végrehajtott módosítások minden, a felhasználó által `CurrentUser` elindított PowerShell-munkamenetre hatással lesznek.</span><span class="sxs-lookup"><span data-stu-id="f2891-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="f2891-128">Ha egy adott munkamenetnek más beállításokat kell használnia, használja a `Process` hatókört.</span><span class="sxs-lookup"><span data-stu-id="f2891-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

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

### <span data-ttu-id="f2891-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2891-129">-Confirm</span></span>

<span data-ttu-id="f2891-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f2891-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2891-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2891-131">-WhatIf</span></span>

<span data-ttu-id="f2891-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f2891-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2891-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f2891-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="f2891-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2891-134">CommonParameters</span></span>
<span data-ttu-id="f2891-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2891-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2891-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2891-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2891-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2891-137">INPUTS</span></span>

### <span data-ttu-id="f2891-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="f2891-138">None</span></span>

## <span data-ttu-id="f2891-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2891-139">OUTPUTS</span></span>

### <span data-ttu-id="f2891-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="f2891-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="f2891-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2891-141">NOTES</span></span>

## <span data-ttu-id="f2891-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2891-142">RELATED LINKS</span></span>
