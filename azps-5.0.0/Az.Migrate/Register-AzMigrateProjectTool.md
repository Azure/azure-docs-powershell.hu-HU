---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194343"
---
# <span data-ttu-id="262a5-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="262a5-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="262a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="262a5-102">SYNOPSIS</span></span>
<span data-ttu-id="262a5-103">Eszköz regisztrálása az áttelepítési projektben.</span><span class="sxs-lookup"><span data-stu-id="262a5-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="262a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="262a5-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="262a5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="262a5-105">DESCRIPTION</span></span>
<span data-ttu-id="262a5-106">Eszköz regisztrálása az áttelepítési projektben.</span><span class="sxs-lookup"><span data-stu-id="262a5-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="262a5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="262a5-107">EXAMPLES</span></span>

### <span data-ttu-id="262a5-108">Példa 1: REgister Tool.</span><span class="sxs-lookup"><span data-stu-id="262a5-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="262a5-109">Eszköz regisztrálása az áttelepítési projektben.</span><span class="sxs-lookup"><span data-stu-id="262a5-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="262a5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="262a5-110">PARAMETERS</span></span>

### <span data-ttu-id="262a5-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="262a5-111">-AcceptLanguage</span></span>
<span data-ttu-id="262a5-112">Szokásos kérés fejléce</span><span class="sxs-lookup"><span data-stu-id="262a5-112">Standard request header.</span></span>
<span data-ttu-id="262a5-113">A szolgáltatás a megfelelő nyelven válaszol az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="262a5-113">Used by service to respond to client in appropriate language.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262a5-114">-DefaultProfile</span></span>
<span data-ttu-id="262a5-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="262a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a5-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="262a5-116">-MigrateProjectName</span></span>
<span data-ttu-id="262a5-117">Az Azure áttelepítési projekt neve.</span><span class="sxs-lookup"><span data-stu-id="262a5-117">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="262a5-118">-ResourceGroupName</span></span>
<span data-ttu-id="262a5-119">Annak a programnak a neve, amely a projectet Áttelepítő Azure Resource Group része.</span><span class="sxs-lookup"><span data-stu-id="262a5-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a5-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="262a5-120">-SubscriptionId</span></span>
<span data-ttu-id="262a5-121">Azure-előfizetési azonosító, amelybe a projekt-áttelepítést hozta létre.</span><span class="sxs-lookup"><span data-stu-id="262a5-121">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a5-122">-Eszköz</span><span class="sxs-lookup"><span data-stu-id="262a5-122">-Tool</span></span>
<span data-ttu-id="262a5-123">Beadja vagy beállítja a regisztrálni kívánt eszközt.</span><span class="sxs-lookup"><span data-stu-id="262a5-123">Gets or sets the tool to be registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a5-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="262a5-124">-Confirm</span></span>
<span data-ttu-id="262a5-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="262a5-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="262a5-126">-WhatIf</span></span>
<span data-ttu-id="262a5-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="262a5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="262a5-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="262a5-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262a5-129">CommonParameters</span></span>
<span data-ttu-id="262a5-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="262a5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262a5-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="262a5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262a5-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="262a5-132">INPUTS</span></span>

## <span data-ttu-id="262a5-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="262a5-133">OUTPUTS</span></span>

### <span data-ttu-id="262a5-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="262a5-134">System.Boolean</span></span>

## <span data-ttu-id="262a5-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="262a5-135">NOTES</span></span>

<span data-ttu-id="262a5-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="262a5-136">ALIASES</span></span>

## <span data-ttu-id="262a5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="262a5-137">RELATED LINKS</span></span>

