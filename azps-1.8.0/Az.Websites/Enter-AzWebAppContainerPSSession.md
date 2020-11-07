---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: b18008268ffd07369cf527c53d6ad693a38d85f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668377"
---
# <span data-ttu-id="966a5-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="966a5-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="966a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="966a5-102">SYNOPSIS</span></span>
<span data-ttu-id="966a5-103">Távoli PowerShell-munkamenet megnyitása egy adott webhelyen vagy a bővítőhelyen és az adott erőforráscsoporthoz megadott Windows-tárolóban</span><span class="sxs-lookup"><span data-stu-id="966a5-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="966a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="966a5-104">SYNTAX</span></span>

### <span data-ttu-id="966a5-105">S1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="966a5-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="966a5-106">S2</span><span class="sxs-lookup"><span data-stu-id="966a5-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="966a5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="966a5-107">DESCRIPTION</span></span>
<span data-ttu-id="966a5-108">távoli PowerShell-munkamenet megnyitása egy adott webhelyen vagy a bővítőhelyen és az adott erőforráscsoporthoz megadott Windows-tárolóban</span><span class="sxs-lookup"><span data-stu-id="966a5-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="966a5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="966a5-109">EXAMPLES</span></span>

### <span data-ttu-id="966a5-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="966a5-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="966a5-111">Ez a parancs egy távoli PowerShell-munkamenetet nyit meg a Windows Container app ContosoASP</span><span class="sxs-lookup"><span data-stu-id="966a5-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="966a5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="966a5-112">PARAMETERS</span></span>

### <span data-ttu-id="966a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="966a5-113">-DefaultProfile</span></span>
<span data-ttu-id="966a5-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="966a5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="966a5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="966a5-115">-Force</span></span>
<span data-ttu-id="966a5-116">A PowerShell-munkamenet létrehozása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="966a5-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="966a5-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="966a5-117">-Name</span></span>
<span data-ttu-id="966a5-118">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="966a5-118">The name of the web app.</span></span>

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

### <span data-ttu-id="966a5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="966a5-119">-PassThru</span></span>
<span data-ttu-id="966a5-120">Sikert vagy kudarcot jelző érték visszaadása</span><span class="sxs-lookup"><span data-stu-id="966a5-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="966a5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="966a5-121">-ResourceGroupName</span></span>
<span data-ttu-id="966a5-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="966a5-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="966a5-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="966a5-123">-SlotName</span></span>
<span data-ttu-id="966a5-124">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="966a5-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="966a5-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="966a5-125">-WebApp</span></span>
<span data-ttu-id="966a5-126">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="966a5-126">The web app object</span></span>

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

### <span data-ttu-id="966a5-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="966a5-127">-Confirm</span></span>
<span data-ttu-id="966a5-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="966a5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="966a5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="966a5-129">-WhatIf</span></span>
<span data-ttu-id="966a5-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="966a5-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="966a5-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="966a5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="966a5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="966a5-132">CommonParameters</span></span>
<span data-ttu-id="966a5-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="966a5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="966a5-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="966a5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="966a5-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="966a5-135">INPUTS</span></span>

### <span data-ttu-id="966a5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="966a5-136">System.String</span></span>

### <span data-ttu-id="966a5-137">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="966a5-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="966a5-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="966a5-138">OUTPUTS</span></span>

### <span data-ttu-id="966a5-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="966a5-139">System.Void</span></span>

## <span data-ttu-id="966a5-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="966a5-140">NOTES</span></span>

## <span data-ttu-id="966a5-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="966a5-141">RELATED LINKS</span></span>
