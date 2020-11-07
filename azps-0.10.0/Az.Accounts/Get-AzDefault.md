---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 3e929d2df0b2132b89f6ccff6b83020453b61ad2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841061"
---
# <span data-ttu-id="342b2-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="342b2-101">Get-AzDefault</span></span>

## <span data-ttu-id="342b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="342b2-102">SYNOPSIS</span></span>
<span data-ttu-id="342b2-103">A felhasználó által az aktuális környezetben beállított alapértékek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="342b2-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="342b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="342b2-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="342b2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="342b2-105">DESCRIPTION</span></span>
<span data-ttu-id="342b2-106">A Get-AzDefault parancsmag azt az erőforráscsoportot kapja, amelyet a felhasználó alapértelmezettként beállított az aktuális környezetben.</span><span class="sxs-lookup"><span data-stu-id="342b2-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="342b2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="342b2-107">EXAMPLES</span></span>

### <span data-ttu-id="342b2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="342b2-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="342b2-109">Ez a parancs az aktuális alapértékeket adja eredményül, ha az alapértelmezett beállítás be van állítva, vagy ha nincs alapértelmezett beállítás, akkor a program semmit ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="342b2-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="342b2-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="342b2-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="342b2-111">Ez a parancs az aktuális alapértelmezett erőforráscsoport értékét adja eredményül, ha van alapértelmezett halmaz, vagy ha a program nem ad meg semmit, ha nincs beállítva alapértelmezett beállítás.</span><span class="sxs-lookup"><span data-stu-id="342b2-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="342b2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="342b2-112">PARAMETERS</span></span>

### <span data-ttu-id="342b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342b2-113">-DefaultProfile</span></span>
<span data-ttu-id="342b2-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="342b2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="342b2-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="342b2-115">-ResourceGroup</span></span>
<span data-ttu-id="342b2-116">Az alapértelmezett erőforráscsoport megjelenítése</span><span class="sxs-lookup"><span data-stu-id="342b2-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="342b2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342b2-117">CommonParameters</span></span>
<span data-ttu-id="342b2-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="342b2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342b2-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="342b2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342b2-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="342b2-120">INPUTS</span></span>

### <span data-ttu-id="342b2-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="342b2-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="342b2-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="342b2-122">OUTPUTS</span></span>

### <span data-ttu-id="342b2-123">Microsoft. Azure. Command. profil. models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="342b2-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="342b2-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="342b2-124">NOTES</span></span>

## <span data-ttu-id="342b2-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="342b2-125">RELATED LINKS</span></span>
