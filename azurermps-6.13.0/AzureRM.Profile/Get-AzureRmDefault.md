---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
ms.openlocfilehash: 7430402d62d88ea192b94166f48c0657e47cbf15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672238"
---
# <span data-ttu-id="e1ab9-101">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="e1ab9-101">Get-AzureRmDefault</span></span>

## <span data-ttu-id="e1ab9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1ab9-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ab9-103">A felhasználó által az aktuális környezetben beállított alapértékek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="e1ab9-103">Get the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1ab9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1ab9-104">SYNTAX</span></span>

```
Get-AzureRmDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1ab9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1ab9-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ab9-106">A Get-AzureRmDefault parancsmag azt az erőforráscsoportot kapja, amelyet a felhasználó alapértelmezettként beállított az aktuális környezetben.</span><span class="sxs-lookup"><span data-stu-id="e1ab9-106">The Get-AzureRmDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="e1ab9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e1ab9-107">EXAMPLES</span></span>

### <span data-ttu-id="e1ab9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e1ab9-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="e1ab9-109">Ez a parancs az aktuális alapértékeket adja eredményül, ha az alapértelmezett beállítás be van állítva, vagy ha nincs alapértelmezett beállítás, akkor a program semmit ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="e1ab9-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="e1ab9-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="e1ab9-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="e1ab9-111">Ez a parancs az aktuális alapértelmezett erőforráscsoport értékét adja eredményül, ha van alapértelmezett halmaz, vagy ha a program nem ad meg semmit, ha nincs beállítva alapértelmezett beállítás.</span><span class="sxs-lookup"><span data-stu-id="e1ab9-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="e1ab9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1ab9-112">PARAMETERS</span></span>

### <span data-ttu-id="e1ab9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ab9-113">-DefaultProfile</span></span>
<span data-ttu-id="e1ab9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1ab9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1ab9-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e1ab9-115">-ResourceGroup</span></span>
<span data-ttu-id="e1ab9-116">Az alapértelmezett erőforráscsoport megjelenítése</span><span class="sxs-lookup"><span data-stu-id="e1ab9-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="e1ab9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ab9-117">CommonParameters</span></span>
<span data-ttu-id="e1ab9-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1ab9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ab9-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ab9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ab9-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1ab9-120">INPUTS</span></span>

### <span data-ttu-id="e1ab9-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e1ab9-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e1ab9-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1ab9-122">OUTPUTS</span></span>

### <span data-ttu-id="e1ab9-123">Microsoft. Azure. Command. profil. models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e1ab9-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="e1ab9-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1ab9-124">NOTES</span></span>

## <span data-ttu-id="e1ab9-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1ab9-125">RELATED LINKS</span></span>
