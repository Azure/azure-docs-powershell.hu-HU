---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
ms.openlocfilehash: 20d66412002e8feb1b4007608091cdbf0422b6c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502539"
---
# <span data-ttu-id="aea91-101">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="aea91-101">Get-AzureRmDefault</span></span>

## <span data-ttu-id="aea91-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aea91-102">SYNOPSIS</span></span>
<span data-ttu-id="aea91-103">A felhasználó által az aktuális környezetben beállított alapértékek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="aea91-103">Get the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aea91-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aea91-104">SYNTAX</span></span>

```
Get-AzureRmDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aea91-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aea91-105">DESCRIPTION</span></span>
<span data-ttu-id="aea91-106">A Get-AzureRmDefault parancsmag azt az erőforráscsoportot kapja, amelyet a felhasználó alapértelmezettként beállított az aktuális környezetben.</span><span class="sxs-lookup"><span data-stu-id="aea91-106">The Get-AzureRmDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="aea91-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aea91-107">EXAMPLES</span></span>

### <span data-ttu-id="aea91-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aea91-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="aea91-109">Ez a parancs az aktuális alapértékeket adja eredményül, ha az alapértelmezett beállítás be van állítva, vagy ha nincs alapértelmezett beállítás, akkor a program semmit ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="aea91-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="aea91-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="aea91-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="aea91-111">Ez a parancs az aktuális alapértelmezett erőforráscsoport értékét adja eredményül, ha van alapértelmezett halmaz, vagy ha a program nem ad meg semmit, ha nincs beállítva alapértelmezett beállítás.</span><span class="sxs-lookup"><span data-stu-id="aea91-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="aea91-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aea91-112">PARAMETERS</span></span>

### <span data-ttu-id="aea91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea91-113">-DefaultProfile</span></span>
<span data-ttu-id="aea91-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aea91-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea91-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aea91-115">-ResourceGroup</span></span>
<span data-ttu-id="aea91-116">Az alapértelmezett erőforráscsoport megjelenítése</span><span class="sxs-lookup"><span data-stu-id="aea91-116">Display Default Resource Group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aea91-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea91-117">CommonParameters</span></span>
<span data-ttu-id="aea91-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aea91-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea91-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea91-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea91-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aea91-120">INPUTS</span></span>

### <span data-ttu-id="aea91-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aea91-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aea91-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aea91-122">OUTPUTS</span></span>

### <span data-ttu-id="aea91-123">Microsoft. Azure. Management. internal. Resources. models. ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aea91-123">Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroup</span></span>

## <span data-ttu-id="aea91-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aea91-124">NOTES</span></span>

## <span data-ttu-id="aea91-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aea91-125">RELATED LINKS</span></span>

