---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 007142cb854e2e428983f95d7bb7397c5a0ace39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017961"
---
# <span data-ttu-id="c0813-101">Get-AzAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="c0813-101">Get-AzAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="c0813-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0813-102">SYNOPSIS</span></span>
<span data-ttu-id="c0813-103">Meta-Configuration. MOF fájlokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c0813-103">Creates meta-configuration .mof files.</span></span>

## <span data-ttu-id="c0813-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0813-104">SYNTAX</span></span>

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0813-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0813-105">DESCRIPTION</span></span>
<span data-ttu-id="c0813-106">A **Get-AzAutomationDscOnboardingMetaconfig** PARANCSMAG az APS-hez szükséges állapot-konfiguráció (DSC) meta-konfigurációjának (MOF) fájljait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c0813-106">The **Get-AzAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="c0813-107">Ez a parancsmag minden megadott számítógépnévhez létrehoz egy. MOF fájlt.</span><span class="sxs-lookup"><span data-stu-id="c0813-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="c0813-108">A parancsmag létrehoz egy mappát a. MOF fájlok számára.</span><span class="sxs-lookup"><span data-stu-id="c0813-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="c0813-109">A mappa Set-DscLocalConfigurationManager parancsmagját futtathatja a következő számítógépeken az Azure automatizálási fiókba a DSC csomópontok segítségével.</span><span class="sxs-lookup"><span data-stu-id="c0813-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="c0813-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c0813-110">EXAMPLES</span></span>

### <span data-ttu-id="c0813-111">1. példa: fedélzeti kiszolgálók automatizálási DSC-nek</span><span class="sxs-lookup"><span data-stu-id="c0813-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="c0813-112">Az első parancs a DSC meta-konfigurációs fájlokat hozza létre két kiszolgálón a Contoso17 nevű automatizálási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="c0813-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="c0813-113">A parancs a fájlokat egy asztalra menti.</span><span class="sxs-lookup"><span data-stu-id="c0813-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="c0813-114">A második parancs a **set-DscLocalConfigurationManager** parancsmagot használva alkalmazza a meta-konfigurációt a megadott számítógépekre a DSC-csomópontok bevezetéséhez.</span><span class="sxs-lookup"><span data-stu-id="c0813-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="c0813-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0813-115">PARAMETERS</span></span>

### <span data-ttu-id="c0813-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c0813-116">-AutomationAccountName</span></span>
<span data-ttu-id="c0813-117">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0813-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="c0813-118">Azok a számítógépek is bejelentkezhetnek, amelyekben a *számítógépnév* paraméter a paraméter által megadott fiókhoz van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="c0813-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0813-119">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="c0813-119">-ComputerName</span></span>
<span data-ttu-id="c0813-120">Azoknak a számítógépeknek a tömböket adja meg, amelyekhez a parancsmag. MOF fájlokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c0813-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="c0813-121">Ha nem adja meg ezt a paramétert, a parancsmag. MOF fájlt hoz létre az aktuális számítógép (localhost) számára.</span><span class="sxs-lookup"><span data-stu-id="c0813-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0813-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0813-122">-DefaultProfile</span></span>
<span data-ttu-id="c0813-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c0813-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0813-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c0813-124">-Force</span></span>
<span data-ttu-id="c0813-125">Arra kényszeríti a parancsot, hogy ne kérjen megerősítést, és cserélje le a meglévő. MOF fájlokat is.</span><span class="sxs-lookup"><span data-stu-id="c0813-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="c0813-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="c0813-126">-OutputFolder</span></span>
<span data-ttu-id="c0813-127">Annak a mappának a nevét adja meg, ahol a parancsmag. MOF fájlokat tárol.</span><span class="sxs-lookup"><span data-stu-id="c0813-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0813-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0813-128">-ResourceGroupName</span></span>
<span data-ttu-id="c0813-129">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0813-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c0813-130">Ez a parancsmag a. MOF fájlokat hozza létre az erőforráscsoport azon alaplapi számítógépeihez, amelyeket ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="c0813-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0813-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c0813-131">-Confirm</span></span>
<span data-ttu-id="c0813-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0813-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0813-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0813-133">-WhatIf</span></span>
<span data-ttu-id="c0813-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c0813-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0813-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0813-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0813-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0813-136">CommonParameters</span></span>
<span data-ttu-id="c0813-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0813-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0813-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0813-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0813-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0813-139">INPUTS</span></span>

### <span data-ttu-id="c0813-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c0813-140">System.String</span></span>

### <span data-ttu-id="c0813-141">System. string []</span><span class="sxs-lookup"><span data-stu-id="c0813-141">System.String[]</span></span>

## <span data-ttu-id="c0813-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0813-142">OUTPUTS</span></span>

### <span data-ttu-id="c0813-143">Microsoft. Azure. Command. Automation. Model. DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="c0813-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="c0813-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0813-144">NOTES</span></span>

## <span data-ttu-id="c0813-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0813-145">RELATED LINKS</span></span>
