---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 651ca91a8da5a025040127b4e3bbcedf16225faf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668331"
---
# <span data-ttu-id="cdabe-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="cdabe-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="cdabe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cdabe-102">SYNOPSIS</span></span>
<span data-ttu-id="cdabe-103">New-AzWebAppContainerPSSession új távoli PowerShell-munkamenetet hoz létre egy adott webhelyen vagy bővítőhelyen vagy erőforrás csoportban megadott Windows-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="cdabe-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="cdabe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cdabe-104">SYNTAX</span></span>

### <span data-ttu-id="cdabe-105">S1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cdabe-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdabe-106">S2</span><span class="sxs-lookup"><span data-stu-id="cdabe-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdabe-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cdabe-107">DESCRIPTION</span></span>
<span data-ttu-id="cdabe-108">New-AzWebAppContainerPSSession új távoli PowerShell-munkamenetet hoz létre egy adott webhelyen vagy bővítőhelyen vagy erőforrás csoportban megadott Windows-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="cdabe-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="cdabe-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cdabe-109">EXAMPLES</span></span>

### <span data-ttu-id="cdabe-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cdabe-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="cdabe-111">Ezzel új távoli PowerShell-munkamenetet hoz létre a Windows Container app ContosoASP, és megjeleníti a tároló ContosoASP futó folyamatokat.</span><span class="sxs-lookup"><span data-stu-id="cdabe-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="cdabe-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cdabe-112">PARAMETERS</span></span>

### <span data-ttu-id="cdabe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdabe-113">-DefaultProfile</span></span>
<span data-ttu-id="cdabe-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdabe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdabe-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cdabe-115">-Force</span></span>
<span data-ttu-id="cdabe-116">A PowerShell-munkamenet létrehozása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="cdabe-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cdabe-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cdabe-117">-Name</span></span>
<span data-ttu-id="cdabe-118">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="cdabe-118">The name of the web app.</span></span>

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

### <span data-ttu-id="cdabe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdabe-119">-ResourceGroupName</span></span>
<span data-ttu-id="cdabe-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cdabe-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="cdabe-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="cdabe-121">-SlotName</span></span>
<span data-ttu-id="cdabe-122">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="cdabe-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="cdabe-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cdabe-123">-WebApp</span></span>
<span data-ttu-id="cdabe-124">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="cdabe-124">The web app object</span></span>

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

### <span data-ttu-id="cdabe-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cdabe-125">-Confirm</span></span>
<span data-ttu-id="cdabe-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cdabe-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdabe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdabe-127">-WhatIf</span></span>
<span data-ttu-id="cdabe-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cdabe-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdabe-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cdabe-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdabe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdabe-130">CommonParameters</span></span>
<span data-ttu-id="cdabe-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cdabe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdabe-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdabe-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdabe-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdabe-133">INPUTS</span></span>

### <span data-ttu-id="cdabe-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cdabe-134">System.String</span></span>

### <span data-ttu-id="cdabe-135">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="cdabe-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cdabe-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdabe-136">OUTPUTS</span></span>

### <span data-ttu-id="cdabe-137">System. Management. Automation. Runspaces. PSSession</span><span class="sxs-lookup"><span data-stu-id="cdabe-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="cdabe-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cdabe-138">NOTES</span></span>

## <span data-ttu-id="cdabe-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdabe-139">RELATED LINKS</span></span>
