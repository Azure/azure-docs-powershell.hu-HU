---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194338"
---
# <span data-ttu-id="d57d5-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="d57d5-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="d57d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d57d5-102">SYNOPSIS</span></span>
<span data-ttu-id="d57d5-103">Törölje az áttelepítési projektet.</span><span class="sxs-lookup"><span data-stu-id="d57d5-103">Delete the migrate project.</span></span>
<span data-ttu-id="d57d5-104">A nem létező projektek törlése nem működik.</span><span class="sxs-lookup"><span data-stu-id="d57d5-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="d57d5-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d57d5-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d57d5-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="d57d5-106">DESCRIPTION</span></span>
<span data-ttu-id="d57d5-107">Törölje az áttelepítési projektet.</span><span class="sxs-lookup"><span data-stu-id="d57d5-107">Delete the migrate project.</span></span>
<span data-ttu-id="d57d5-108">A nem létező projektek törlése nem működik.</span><span class="sxs-lookup"><span data-stu-id="d57d5-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="d57d5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d57d5-109">EXAMPLES</span></span>

### <span data-ttu-id="d57d5-110">Példa 1: delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d57d5-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="d57d5-111">Törölje az áttelepítési projektet.</span><span class="sxs-lookup"><span data-stu-id="d57d5-111">Delete the migrate project.</span></span>
<span data-ttu-id="d57d5-112">A nem létező projektek törlése nem működik.</span><span class="sxs-lookup"><span data-stu-id="d57d5-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="d57d5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d57d5-113">PARAMETERS</span></span>

### <span data-ttu-id="d57d5-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="d57d5-114">-AcceptLanguage</span></span>
<span data-ttu-id="d57d5-115">Szokásos kérés fejléce</span><span class="sxs-lookup"><span data-stu-id="d57d5-115">Standard request header.</span></span>
<span data-ttu-id="d57d5-116">A szolgáltatás a megfelelő nyelven válaszol az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="d57d5-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="d57d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d57d5-117">-DefaultProfile</span></span>
<span data-ttu-id="d57d5-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d57d5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d57d5-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d57d5-119">-Name</span></span>
<span data-ttu-id="d57d5-120">Az Azure áttelepítési projekt neve.</span><span class="sxs-lookup"><span data-stu-id="d57d5-120">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57d5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d57d5-121">-PassThru</span></span>
<span data-ttu-id="d57d5-122">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="d57d5-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57d5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d57d5-123">-ResourceGroupName</span></span>
<span data-ttu-id="d57d5-124">Annak a programnak a neve, amely a projectet Áttelepítő Azure Resource Group része.</span><span class="sxs-lookup"><span data-stu-id="d57d5-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="d57d5-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d57d5-125">-SubscriptionId</span></span>
<span data-ttu-id="d57d5-126">Azure-előfizetési azonosító, amelybe a projekt-áttelepítést hozta létre.</span><span class="sxs-lookup"><span data-stu-id="d57d5-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="d57d5-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d57d5-127">-Confirm</span></span>
<span data-ttu-id="d57d5-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d57d5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d57d5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d57d5-129">-WhatIf</span></span>
<span data-ttu-id="d57d5-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d57d5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d57d5-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d57d5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d57d5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57d5-132">CommonParameters</span></span>
<span data-ttu-id="d57d5-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d57d5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57d5-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d57d5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57d5-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d57d5-135">INPUTS</span></span>

## <span data-ttu-id="d57d5-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d57d5-136">OUTPUTS</span></span>

### <span data-ttu-id="d57d5-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d57d5-137">System.Boolean</span></span>

## <span data-ttu-id="d57d5-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d57d5-138">NOTES</span></span>

<span data-ttu-id="d57d5-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d57d5-139">ALIASES</span></span>

## <span data-ttu-id="d57d5-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d57d5-140">RELATED LINKS</span></span>

