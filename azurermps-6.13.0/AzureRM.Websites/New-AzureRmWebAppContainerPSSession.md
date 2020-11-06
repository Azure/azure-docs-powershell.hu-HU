---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 3c5efcd51a8b546acb5fa9b8ed3623c40ddfb1e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492661"
---
# <span data-ttu-id="e2018-101">New-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="e2018-101">New-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="e2018-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2018-102">SYNOPSIS</span></span>
<span data-ttu-id="e2018-103">New-AzureRmWebAppContainerPSSession új távoli PowerShell-munkamenetet hoz létre egy adott webhelyen vagy bővítőhelyen vagy erőforrás csoportban megadott Windows-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="e2018-103">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2018-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2018-104">SYNTAX</span></span>

### <span data-ttu-id="e2018-105">S1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2018-105">S1 (Default)</span></span>
```
New-AzureRmWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2018-106">S2</span><span class="sxs-lookup"><span data-stu-id="e2018-106">S2</span></span>
```
New-AzureRmWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2018-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2018-107">DESCRIPTION</span></span>
<span data-ttu-id="e2018-108">New-AzureRmWebAppContainerPSSession új távoli PowerShell-munkamenetet hoz létre egy adott webhelyen vagy bővítőhelyen vagy erőforrás csoportban megadott Windows-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="e2018-108">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="e2018-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e2018-109">EXAMPLES</span></span>

### <span data-ttu-id="e2018-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e2018-110">Example 1</span></span>
```
PS C:\> $s = New-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="e2018-111">Ezzel új távoli PowerShell-munkamenetet hoz létre a Windows Container app ContosoASP, és megjeleníti a tároló ContosoASP futó folyamatokat.</span><span class="sxs-lookup"><span data-stu-id="e2018-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="e2018-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2018-112">PARAMETERS</span></span>

### <span data-ttu-id="e2018-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2018-113">-DefaultProfile</span></span>
<span data-ttu-id="e2018-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2018-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2018-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e2018-115">-Force</span></span>
<span data-ttu-id="e2018-116">A PowerShell-munkamenet létrehozása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="e2018-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e2018-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2018-117">-Name</span></span>
<span data-ttu-id="e2018-118">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="e2018-118">The name of the web app.</span></span>

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

### <span data-ttu-id="e2018-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2018-119">-ResourceGroupName</span></span>
<span data-ttu-id="e2018-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e2018-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="e2018-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="e2018-121">-SlotName</span></span>
<span data-ttu-id="e2018-122">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="e2018-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="e2018-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e2018-123">-WebApp</span></span>
<span data-ttu-id="e2018-124">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="e2018-124">The web app object</span></span>

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

### <span data-ttu-id="e2018-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e2018-125">-Confirm</span></span>
<span data-ttu-id="e2018-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2018-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2018-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2018-127">-WhatIf</span></span>
<span data-ttu-id="e2018-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e2018-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2018-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2018-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2018-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2018-130">CommonParameters</span></span>
<span data-ttu-id="e2018-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2018-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2018-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2018-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2018-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2018-133">INPUTS</span></span>

### <span data-ttu-id="e2018-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e2018-134">System.String</span></span>
### <span data-ttu-id="e2018-135">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e2018-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="e2018-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2018-136">OUTPUTS</span></span>

### <span data-ttu-id="e2018-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e2018-137">System.String</span></span>
## <span data-ttu-id="e2018-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2018-138">NOTES</span></span>

## <span data-ttu-id="e2018-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2018-139">RELATED LINKS</span></span>
