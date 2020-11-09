---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301820"
---
# <span data-ttu-id="74f72-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="74f72-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="74f72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74f72-102">SYNOPSIS</span></span>
<span data-ttu-id="74f72-103">Egy Azure-SecurityPartnerProvider törlése</span><span class="sxs-lookup"><span data-stu-id="74f72-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="74f72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74f72-104">SYNTAX</span></span>

### <span data-ttu-id="74f72-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f72-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f72-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f72-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f72-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f72-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74f72-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="74f72-108">DESCRIPTION</span></span>
<span data-ttu-id="74f72-109">A **Remove-AzSecurityPartnerProvider** parancsmag töröl egy Azure-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="74f72-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="74f72-110">Példák</span><span class="sxs-lookup"><span data-stu-id="74f72-110">EXAMPLES</span></span>

### <span data-ttu-id="74f72-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="74f72-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="74f72-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74f72-112">PARAMETERS</span></span>

### <span data-ttu-id="74f72-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74f72-113">-AsJob</span></span>
<span data-ttu-id="74f72-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="74f72-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74f72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f72-115">-DefaultProfile</span></span>
<span data-ttu-id="74f72-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74f72-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74f72-117">-Force</span><span class="sxs-lookup"><span data-stu-id="74f72-117">-Force</span></span>
<span data-ttu-id="74f72-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74f72-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="74f72-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="74f72-119">-Name</span></span>
<span data-ttu-id="74f72-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="74f72-120">The resource name.</span></span>

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

### <span data-ttu-id="74f72-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74f72-121">-PassThru</span></span>
<span data-ttu-id="74f72-122">Egy olyan objektumot ad eredményül, amely azt az elemet jeleníti meg, amelyen a művelet végre van hajtva.</span><span class="sxs-lookup"><span data-stu-id="74f72-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="74f72-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74f72-123">-ResourceGroupName</span></span>
<span data-ttu-id="74f72-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="74f72-124">The resource group name.</span></span>

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

### <span data-ttu-id="74f72-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74f72-125">-ResourceId</span></span>
<span data-ttu-id="74f72-126">A securityPartnerProvider erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="74f72-126">The securityPartnerProvider resource Id.</span></span>

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

### <span data-ttu-id="74f72-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="74f72-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="74f72-128">A securityPartnerProvider bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="74f72-128">The securityPartnerProvider input object.</span></span>

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

### <span data-ttu-id="74f72-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="74f72-129">-Confirm</span></span>
<span data-ttu-id="74f72-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74f72-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74f72-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74f72-131">-WhatIf</span></span>
<span data-ttu-id="74f72-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="74f72-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74f72-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74f72-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74f72-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f72-134">CommonParameters</span></span>
<span data-ttu-id="74f72-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74f72-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f72-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="74f72-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f72-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74f72-137">INPUTS</span></span>

### <span data-ttu-id="74f72-138">System. String</span><span class="sxs-lookup"><span data-stu-id="74f72-138">System.String</span></span>

### <span data-ttu-id="74f72-139">Microsoft. Azure. commands. Network. models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="74f72-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="74f72-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74f72-140">OUTPUTS</span></span>

### <span data-ttu-id="74f72-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74f72-141">System.Boolean</span></span>

## <span data-ttu-id="74f72-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74f72-142">NOTES</span></span>

## <span data-ttu-id="74f72-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74f72-143">RELATED LINKS</span></span>
