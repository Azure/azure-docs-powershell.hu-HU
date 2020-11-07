---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 8abb473eb5def0d2ca360e0b6116069aecc21b16
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841006"
---
# <span data-ttu-id="31489-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="31489-101">Set-AzDefault</span></span>

## <span data-ttu-id="31489-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31489-102">SYNOPSIS</span></span>
<span data-ttu-id="31489-103">Alapértelmezett érték beállítása az aktuális környezetben</span><span class="sxs-lookup"><span data-stu-id="31489-103">Sets a default in the current context</span></span>

## <span data-ttu-id="31489-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31489-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31489-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="31489-105">DESCRIPTION</span></span>
<span data-ttu-id="31489-106">Az Set-AzDefault parancsmag az aktuális környezetben az alapértelmezett beállításokat adja meg vagy módosítja.</span><span class="sxs-lookup"><span data-stu-id="31489-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="31489-107">Példák</span><span class="sxs-lookup"><span data-stu-id="31489-107">EXAMPLES</span></span>

### <span data-ttu-id="31489-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="31489-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="31489-109">Ez a parancs beállítja az alapértelmezett erőforrás csoportot a felhasználó által megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="31489-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="31489-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31489-110">PARAMETERS</span></span>

### <span data-ttu-id="31489-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31489-111">-DefaultProfile</span></span>
<span data-ttu-id="31489-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31489-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31489-113">-Force</span><span class="sxs-lookup"><span data-stu-id="31489-113">-Force</span></span>
<span data-ttu-id="31489-114">Új erőforráscsoport létrehozása, ha a megadott alapértelmezett érték nem létezik</span><span class="sxs-lookup"><span data-stu-id="31489-114">Create a new resource group if specified default does not exist</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31489-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31489-115">-ResourceGroupName</span></span>
<span data-ttu-id="31489-116">Az alapértelmezettként beállított erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="31489-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31489-117">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="31489-117">-Scope</span></span>
<span data-ttu-id="31489-118">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="31489-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="31489-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="31489-119">-Confirm</span></span>
<span data-ttu-id="31489-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="31489-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31489-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31489-121">-WhatIf</span></span>
<span data-ttu-id="31489-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="31489-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31489-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="31489-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31489-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31489-124">CommonParameters</span></span>
<span data-ttu-id="31489-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31489-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31489-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="31489-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31489-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31489-127">INPUTS</span></span>

### <span data-ttu-id="31489-128">System. String</span><span class="sxs-lookup"><span data-stu-id="31489-128">System.String</span></span>

## <span data-ttu-id="31489-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31489-129">OUTPUTS</span></span>

### <span data-ttu-id="31489-130">Microsoft. Azure. Command. profil. models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="31489-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="31489-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31489-131">NOTES</span></span>

## <span data-ttu-id="31489-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31489-132">RELATED LINKS</span></span>
