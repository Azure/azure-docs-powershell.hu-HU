---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/remove-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 8b533f26b7fa947a185ee0be2dc5a395e77ebbbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497616"
---
# <span data-ttu-id="64b98-101">Remove-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="64b98-101">Remove-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="64b98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64b98-102">SYNOPSIS</span></span>
<span data-ttu-id="64b98-103">Felhasználó által kiosztott identitás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="64b98-103">Removes a User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64b98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64b98-104">SYNTAX</span></span>

### <span data-ttu-id="64b98-105">ResourceGroupAndNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64b98-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64b98-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b98-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64b98-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b98-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64b98-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="64b98-108">DESCRIPTION</span></span>
<span data-ttu-id="64b98-109">A **Remove-AzureRmUserAssignedIdentity** törli a megadott felhasználó által kiosztott identitást.</span><span class="sxs-lookup"><span data-stu-id="64b98-109">The **Remove-AzureRmUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="64b98-110">Példák</span><span class="sxs-lookup"><span data-stu-id="64b98-110">EXAMPLES</span></span>

### <span data-ttu-id="64b98-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="64b98-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="64b98-112">Ez a példa parancsmag törli az identitás **ID1** az erőforráscsoport **PSRG** csoportban.</span><span class="sxs-lookup"><span data-stu-id="64b98-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>

<span data-ttu-id="64b98-113">Igaz</span><span class="sxs-lookup"><span data-stu-id="64b98-113">True</span></span>

## <span data-ttu-id="64b98-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64b98-114">PARAMETERS</span></span>

### <span data-ttu-id="64b98-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64b98-115">-AsJob</span></span>
<span data-ttu-id="64b98-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="64b98-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64b98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b98-117">-DefaultProfile</span></span>
<span data-ttu-id="64b98-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64b98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64b98-119">-Force</span><span class="sxs-lookup"><span data-stu-id="64b98-119">-Force</span></span>
<span data-ttu-id="64b98-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="64b98-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="64b98-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64b98-121">-InputObject</span></span>
<span data-ttu-id="64b98-122">Az identitás objektum.</span><span class="sxs-lookup"><span data-stu-id="64b98-122">The Identity object.</span></span>

```yaml
Type: PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64b98-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64b98-123">-Name</span></span>
<span data-ttu-id="64b98-124">Az identitás neve.</span><span class="sxs-lookup"><span data-stu-id="64b98-124">The Identity name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b98-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b98-125">-ResourceGroupName</span></span>
<span data-ttu-id="64b98-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="64b98-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b98-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64b98-127">-ResourceId</span></span>
<span data-ttu-id="64b98-128">Az identitás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64b98-128">The Identity's resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b98-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64b98-129">-Confirm</span></span>
<span data-ttu-id="64b98-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64b98-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64b98-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64b98-131">-WhatIf</span></span>
<span data-ttu-id="64b98-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64b98-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64b98-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64b98-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64b98-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b98-134">CommonParameters</span></span>
<span data-ttu-id="64b98-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64b98-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b98-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64b98-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b98-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64b98-137">INPUTS</span></span>

### <span data-ttu-id="64b98-138">System. String</span><span class="sxs-lookup"><span data-stu-id="64b98-138">System.String</span></span>

## <span data-ttu-id="64b98-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64b98-139">OUTPUTS</span></span>

### <span data-ttu-id="64b98-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64b98-140">System.Boolean</span></span>

## <span data-ttu-id="64b98-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64b98-141">NOTES</span></span>

## <span data-ttu-id="64b98-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64b98-142">RELATED LINKS</span></span>
