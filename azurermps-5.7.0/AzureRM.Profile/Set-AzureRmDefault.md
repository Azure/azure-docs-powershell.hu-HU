---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
ms.openlocfilehash: 01b8283277c1d9592adbd8edfe6b883a4451ded9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678959"
---
# <span data-ttu-id="b6e59-101">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="b6e59-101">Set-AzureRmDefault</span></span>

## <span data-ttu-id="b6e59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6e59-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e59-103">Alapértelmezett érték beállítása az aktuális környezetben</span><span class="sxs-lookup"><span data-stu-id="b6e59-103">Sets a default in the current context</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6e59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6e59-104">SYNTAX</span></span>

```
Set-AzureRmDefault [-ResourceGroupName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6e59-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6e59-105">DESCRIPTION</span></span>
<span data-ttu-id="b6e59-106">Az Set-AzureRmDefault parancsmag az aktuális környezetben az alapértelmezett beállításokat adja meg vagy módosítja.</span><span class="sxs-lookup"><span data-stu-id="b6e59-106">The Set-AzureRmDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="b6e59-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b6e59-107">EXAMPLES</span></span>

### <span data-ttu-id="b6e59-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b6e59-108">Example 1</span></span>
```
PS C:\> Set-AzureRmDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="b6e59-109">Ez a parancs beállítja az alapértelmezett erőforrás csoportot a felhasználó által megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="b6e59-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="b6e59-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6e59-110">PARAMETERS</span></span>

### <span data-ttu-id="b6e59-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e59-111">-DefaultProfile</span></span>
<span data-ttu-id="b6e59-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6e59-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6e59-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b6e59-113">-Force</span></span>
<span data-ttu-id="b6e59-114">Új erőforráscsoport létrehozása, ha a megadott alapértelmezett érték nem létezik</span><span class="sxs-lookup"><span data-stu-id="b6e59-114">Create a new resource group if specified default does not exist</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e59-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6e59-115">-ResourceGroupName</span></span>
<span data-ttu-id="b6e59-116">Az alapértelmezettként beállított erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b6e59-116">Name of the resource group being set as default</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e59-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6e59-117">-Confirm</span></span>
<span data-ttu-id="b6e59-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6e59-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e59-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6e59-119">-WhatIf</span></span>
<span data-ttu-id="b6e59-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6e59-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6e59-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6e59-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e59-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e59-122">CommonParameters</span></span>
<span data-ttu-id="b6e59-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6e59-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e59-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6e59-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e59-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6e59-125">INPUTS</span></span>

### <span data-ttu-id="b6e59-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b6e59-126">System.String</span></span>

## <span data-ttu-id="b6e59-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6e59-127">OUTPUTS</span></span>

### <span data-ttu-id="b6e59-128">Microsoft. Azure. Management. internal. Resources. models. ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b6e59-128">Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroup</span></span>

## <span data-ttu-id="b6e59-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6e59-129">NOTES</span></span>

## <span data-ttu-id="b6e59-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6e59-130">RELATED LINKS</span></span>

