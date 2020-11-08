---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: ddf728a1340d763c1feb2ba313a2dc73494b5d30
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187956"
---
# <span data-ttu-id="a588d-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="a588d-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="a588d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a588d-102">SYNOPSIS</span></span>
<span data-ttu-id="a588d-103">Távoli PowerShell-munkamenet megnyitása egy adott webhelyen vagy a bővítőhelyen és az adott erőforráscsoporthoz megadott Windows-tárolóban</span><span class="sxs-lookup"><span data-stu-id="a588d-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="a588d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a588d-104">SYNTAX</span></span>

### <span data-ttu-id="a588d-105">S1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a588d-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a588d-106">S2</span><span class="sxs-lookup"><span data-stu-id="a588d-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a588d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a588d-107">DESCRIPTION</span></span>
<span data-ttu-id="a588d-108">távoli PowerShell-munkamenet megnyitása egy adott webhelyen vagy a bővítőhelyen és az adott erőforráscsoporthoz megadott Windows-tárolóban</span><span class="sxs-lookup"><span data-stu-id="a588d-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="a588d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a588d-109">EXAMPLES</span></span>

### <span data-ttu-id="a588d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a588d-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="a588d-111">Ez a parancs egy távoli PowerShell-munkamenetet nyit meg a Windows Container app ContosoASP</span><span class="sxs-lookup"><span data-stu-id="a588d-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="a588d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a588d-112">PARAMETERS</span></span>

### <span data-ttu-id="a588d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a588d-113">-DefaultProfile</span></span>
<span data-ttu-id="a588d-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a588d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a588d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a588d-115">-Force</span></span>
<span data-ttu-id="a588d-116">A PowerShell-munkamenet létrehozása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="a588d-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a588d-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a588d-117">-Name</span></span>
<span data-ttu-id="a588d-118">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="a588d-118">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a588d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a588d-119">-PassThru</span></span>
<span data-ttu-id="a588d-120">Sikert vagy kudarcot jelző érték visszaadása</span><span class="sxs-lookup"><span data-stu-id="a588d-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="a588d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a588d-121">-ResourceGroupName</span></span>
<span data-ttu-id="a588d-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a588d-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a588d-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="a588d-123">-SlotName</span></span>
<span data-ttu-id="a588d-124">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="a588d-124">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a588d-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a588d-125">-WebApp</span></span>
<span data-ttu-id="a588d-126">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="a588d-126">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a588d-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a588d-127">-Confirm</span></span>
<span data-ttu-id="a588d-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a588d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a588d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a588d-129">-WhatIf</span></span>
<span data-ttu-id="a588d-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a588d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a588d-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a588d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a588d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a588d-132">CommonParameters</span></span>
<span data-ttu-id="a588d-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a588d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a588d-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a588d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a588d-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a588d-135">INPUTS</span></span>

### <span data-ttu-id="a588d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a588d-136">System.String</span></span>

### <span data-ttu-id="a588d-137">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a588d-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a588d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a588d-138">OUTPUTS</span></span>

### <span data-ttu-id="a588d-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="a588d-139">System.Void</span></span>

## <span data-ttu-id="a588d-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a588d-140">NOTES</span></span>

## <span data-ttu-id="a588d-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a588d-141">RELATED LINKS</span></span>
