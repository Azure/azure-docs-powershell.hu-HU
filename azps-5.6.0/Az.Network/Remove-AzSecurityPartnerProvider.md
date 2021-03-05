---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: 3fda360369615c28647769e6bc5aeb0af71e0e35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006166"
---
# <span data-ttu-id="154c2-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="154c2-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="154c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="154c2-102">SYNOPSIS</span></span>
<span data-ttu-id="154c2-103">Egy Azure SecurityPartnerProvider törlése.</span><span class="sxs-lookup"><span data-stu-id="154c2-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="154c2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="154c2-104">SYNTAX</span></span>

### <span data-ttu-id="154c2-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="154c2-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="154c2-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="154c2-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="154c2-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="154c2-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="154c2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="154c2-108">DESCRIPTION</span></span>
<span data-ttu-id="154c2-109">A **Remove-AzSecurityPartnerProvider** parancsmag töröl egy Azure SecurityPartnerProvider-t</span><span class="sxs-lookup"><span data-stu-id="154c2-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="154c2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="154c2-110">EXAMPLES</span></span>

### <span data-ttu-id="154c2-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="154c2-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="154c2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="154c2-112">PARAMETERS</span></span>

### <span data-ttu-id="154c2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="154c2-113">-AsJob</span></span>
<span data-ttu-id="154c2-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="154c2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="154c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="154c2-115">-DefaultProfile</span></span>
<span data-ttu-id="154c2-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="154c2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154c2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="154c2-117">-Force</span></span>
<span data-ttu-id="154c2-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="154c2-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="154c2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="154c2-119">-Name</span></span>
<span data-ttu-id="154c2-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="154c2-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="154c2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="154c2-121">-PassThru</span></span>
<span data-ttu-id="154c2-122">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amelyen a műveletet végre kell hajtanunk.</span><span class="sxs-lookup"><span data-stu-id="154c2-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="154c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="154c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="154c2-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="154c2-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="154c2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="154c2-125">-ResourceId</span></span>
<span data-ttu-id="154c2-126">The securityPartnerProvider resource Id.</span><span class="sxs-lookup"><span data-stu-id="154c2-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="154c2-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="154c2-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="154c2-128">The securityPartnerProvider input object.</span><span class="sxs-lookup"><span data-stu-id="154c2-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="154c2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="154c2-129">-Confirm</span></span>
<span data-ttu-id="154c2-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="154c2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="154c2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="154c2-131">-WhatIf</span></span>
<span data-ttu-id="154c2-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="154c2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="154c2-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="154c2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="154c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="154c2-134">CommonParameters</span></span>
<span data-ttu-id="154c2-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="154c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="154c2-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="154c2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="154c2-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="154c2-137">INPUTS</span></span>

### <span data-ttu-id="154c2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="154c2-138">System.String</span></span>

### <span data-ttu-id="154c2-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="154c2-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="154c2-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="154c2-140">OUTPUTS</span></span>

### <span data-ttu-id="154c2-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="154c2-141">System.Boolean</span></span>

## <span data-ttu-id="154c2-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="154c2-142">NOTES</span></span>

## <span data-ttu-id="154c2-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="154c2-143">RELATED LINKS</span></span>
