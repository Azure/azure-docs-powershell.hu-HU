---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 43806326f572030997299353cfc7e79e5587a4ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479161"
---
# <span data-ttu-id="25aff-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="25aff-101">Get-AzDefault</span></span>

## <span data-ttu-id="25aff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25aff-102">SYNOPSIS</span></span>
<span data-ttu-id="25aff-103">Szerezze be a felhasználó által az aktuális környezetben beállított alapértelmezett értékeket.</span><span class="sxs-lookup"><span data-stu-id="25aff-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="25aff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="25aff-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25aff-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="25aff-105">DESCRIPTION</span></span>
<span data-ttu-id="25aff-106">A Get-AzDefault parancsmag az aktuális környezetben a felhasználó által alapértelmezettként beállított erőforráscsoportot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="25aff-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="25aff-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="25aff-107">EXAMPLES</span></span>

### <span data-ttu-id="25aff-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="25aff-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="25aff-109">Ez a parancs az alapértelmezett beállítások esetén az aktuális alapértékeket adja vissza, illetve ha nincs alapértelmezett beállítás, semmit sem ad vissza.</span><span class="sxs-lookup"><span data-stu-id="25aff-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="25aff-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="25aff-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="25aff-111">Ez a parancs alapértelmezett erőforráscsoport esetén az aktuális alapértelmezett erőforráscsoportot adja vissza, illetve ha nincs alapértelmezett beállítás, semmit sem ad vissza.</span><span class="sxs-lookup"><span data-stu-id="25aff-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="25aff-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25aff-112">PARAMETERS</span></span>

### <span data-ttu-id="25aff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25aff-113">-DefaultProfile</span></span>
<span data-ttu-id="25aff-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25aff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25aff-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="25aff-115">-ResourceGroup</span></span>
<span data-ttu-id="25aff-116">Alapértelmezett erőforráscsoport megjelenítése</span><span class="sxs-lookup"><span data-stu-id="25aff-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="25aff-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25aff-117">CommonParameters</span></span>
<span data-ttu-id="25aff-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25aff-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25aff-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25aff-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25aff-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25aff-120">INPUTS</span></span>

### <span data-ttu-id="25aff-121">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="25aff-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="25aff-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25aff-122">OUTPUTS</span></span>

### <span data-ttu-id="25aff-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="25aff-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="25aff-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="25aff-124">NOTES</span></span>

## <span data-ttu-id="25aff-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25aff-125">RELATED LINKS</span></span>
