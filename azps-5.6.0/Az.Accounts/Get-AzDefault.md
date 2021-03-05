---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: aa1bfb0760480d5c2e24e113653037ecb83a9f6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014421"
---
# <span data-ttu-id="1ef14-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="1ef14-101">Get-AzDefault</span></span>

## <span data-ttu-id="1ef14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ef14-102">SYNOPSIS</span></span>
<span data-ttu-id="1ef14-103">Szerezze be a felhasználó által az aktuális környezetben beállított alapértelmezett értékeket.</span><span class="sxs-lookup"><span data-stu-id="1ef14-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="1ef14-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1ef14-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ef14-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1ef14-105">DESCRIPTION</span></span>
<span data-ttu-id="1ef14-106">A Get-AzDefault parancsmag az aktuális környezetben a felhasználó által alapértelmezettként beállított erőforráscsoportot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1ef14-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="1ef14-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1ef14-107">EXAMPLES</span></span>

### <span data-ttu-id="1ef14-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1ef14-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="1ef14-109">Ez a parancs az alapértelmezett beállítások esetén az aktuális alapértékeket adja vissza, illetve ha nincs alapértelmezett beállítás, semmit sem ad vissza.</span><span class="sxs-lookup"><span data-stu-id="1ef14-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="1ef14-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="1ef14-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="1ef14-111">Ez a parancs alapértelmezett erőforráscsoport esetén az aktuális alapértelmezett erőforráscsoportot adja vissza, illetve ha nincs alapértelmezett beállítás, semmit sem ad vissza.</span><span class="sxs-lookup"><span data-stu-id="1ef14-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="1ef14-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ef14-112">PARAMETERS</span></span>

### <span data-ttu-id="1ef14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ef14-113">-DefaultProfile</span></span>
<span data-ttu-id="1ef14-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ef14-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ef14-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1ef14-115">-ResourceGroup</span></span>
<span data-ttu-id="1ef14-116">Alapértelmezett erőforráscsoport megjelenítése</span><span class="sxs-lookup"><span data-stu-id="1ef14-116">Display Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef14-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ef14-117">CommonParameters</span></span>
<span data-ttu-id="1ef14-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ef14-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ef14-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ef14-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ef14-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ef14-120">INPUTS</span></span>

### <span data-ttu-id="1ef14-121">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1ef14-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1ef14-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ef14-122">OUTPUTS</span></span>

### <span data-ttu-id="1ef14-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1ef14-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="1ef14-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1ef14-124">NOTES</span></span>

## <span data-ttu-id="1ef14-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ef14-125">RELATED LINKS</span></span>
