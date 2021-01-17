---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 43806326f572030997299353cfc7e79e5587a4ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370857"
---
# <span data-ttu-id="8d99d-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="8d99d-101">Get-AzDefault</span></span>

## <span data-ttu-id="8d99d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d99d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d99d-103">Szerezze be a felhasználó által az aktuális környezetben beállított alapértelmezett értékeket.</span><span class="sxs-lookup"><span data-stu-id="8d99d-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="8d99d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d99d-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d99d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d99d-105">DESCRIPTION</span></span>
<span data-ttu-id="8d99d-106">A Get-AzDefault parancsmag az aktuális környezetben a felhasználó által alapértelmezettként beállított erőforráscsoportot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8d99d-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="8d99d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d99d-107">EXAMPLES</span></span>

### <span data-ttu-id="8d99d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8d99d-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="8d99d-109">Ez a parancs az alapértelmezett beállítások esetén az aktuális alapértékeket adja vissza, illetve semmit sem, ha nincs beállítva alapértelmezett beállítás.</span><span class="sxs-lookup"><span data-stu-id="8d99d-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="8d99d-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="8d99d-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="8d99d-111">Ez a parancs alapértelmezett erőforráscsoport esetén az aktuális alapértelmezett erőforráscsoportot adja vissza, illetve ha nincs alapértelmezett beállítás, semmit sem ad vissza.</span><span class="sxs-lookup"><span data-stu-id="8d99d-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="8d99d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d99d-112">PARAMETERS</span></span>

### <span data-ttu-id="8d99d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d99d-113">-DefaultProfile</span></span>
<span data-ttu-id="8d99d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d99d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d99d-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d99d-115">-ResourceGroup</span></span>
<span data-ttu-id="8d99d-116">Alapértelmezett erőforráscsoport megjelenítése</span><span class="sxs-lookup"><span data-stu-id="8d99d-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="8d99d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d99d-117">CommonParameters</span></span>
<span data-ttu-id="8d99d-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d99d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d99d-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d99d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d99d-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d99d-120">INPUTS</span></span>

### <span data-ttu-id="8d99d-121">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8d99d-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8d99d-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d99d-122">OUTPUTS</span></span>

### <span data-ttu-id="8d99d-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d99d-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="8d99d-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d99d-124">NOTES</span></span>

## <span data-ttu-id="8d99d-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d99d-125">RELATED LINKS</span></span>
