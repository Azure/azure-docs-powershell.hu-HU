---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Enter-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Enter-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 350ad76952a2953a107e0626b9cf2e0e8b640bb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492665"
---
# <span data-ttu-id="c6f36-101">Enter-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="c6f36-101">Enter-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="c6f36-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6f36-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f36-103">Távoli PowerShell-munkamenet megnyitása egy adott webhelyen vagy a bővítőhelyen és az adott erőforráscsoporthoz megadott Windows-tárolóban</span><span class="sxs-lookup"><span data-stu-id="c6f36-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6f36-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6f36-104">SYNTAX</span></span>

### <span data-ttu-id="c6f36-105">S1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c6f36-105">S1 (Default)</span></span>
```
Enter-AzureRmWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6f36-106">S2</span><span class="sxs-lookup"><span data-stu-id="c6f36-106">S2</span></span>
```
Enter-AzureRmWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6f36-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6f36-107">DESCRIPTION</span></span>
<span data-ttu-id="c6f36-108">távoli PowerShell-munkamenet megnyitása egy adott webhelyen vagy a bővítőhelyen és az adott erőforráscsoporthoz megadott Windows-tárolóban</span><span class="sxs-lookup"><span data-stu-id="c6f36-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="c6f36-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c6f36-109">EXAMPLES</span></span>

### <span data-ttu-id="c6f36-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c6f36-110">Example 1</span></span>
```
PS C:\> Enter-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="c6f36-111">Ez a parancs egy távoli PowerShell-munkamenetet nyit meg a Windows Container app ContosoASP</span><span class="sxs-lookup"><span data-stu-id="c6f36-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="c6f36-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6f36-112">PARAMETERS</span></span>

### <span data-ttu-id="c6f36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f36-113">-DefaultProfile</span></span>
<span data-ttu-id="c6f36-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6f36-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6f36-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c6f36-115">-Force</span></span>
<span data-ttu-id="c6f36-116">A PowerShell-munkamenet létrehozása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="c6f36-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c6f36-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6f36-117">-Name</span></span>
<span data-ttu-id="c6f36-118">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="c6f36-118">The name of the web app.</span></span>

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

### <span data-ttu-id="c6f36-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6f36-119">-PassThru</span></span>
<span data-ttu-id="c6f36-120">Sikert vagy kudarcot jelző érték visszaadása</span><span class="sxs-lookup"><span data-stu-id="c6f36-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="c6f36-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6f36-121">-ResourceGroupName</span></span>
<span data-ttu-id="c6f36-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c6f36-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="c6f36-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="c6f36-123">-SlotName</span></span>
<span data-ttu-id="c6f36-124">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="c6f36-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="c6f36-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c6f36-125">-WebApp</span></span>
<span data-ttu-id="c6f36-126">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="c6f36-126">The web app object</span></span>

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

### <span data-ttu-id="c6f36-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c6f36-127">-Confirm</span></span>
<span data-ttu-id="c6f36-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c6f36-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6f36-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6f36-129">-WhatIf</span></span>
<span data-ttu-id="c6f36-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c6f36-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6f36-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6f36-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6f36-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f36-132">CommonParameters</span></span>
<span data-ttu-id="c6f36-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6f36-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f36-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6f36-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f36-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6f36-135">INPUTS</span></span>

### <span data-ttu-id="c6f36-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c6f36-136">System.String</span></span>
### <span data-ttu-id="c6f36-137">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c6f36-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="c6f36-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6f36-138">OUTPUTS</span></span>

### <span data-ttu-id="c6f36-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c6f36-139">System.String</span></span>
## <span data-ttu-id="c6f36-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6f36-140">NOTES</span></span>

## <span data-ttu-id="c6f36-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6f36-141">RELATED LINKS</span></span>
