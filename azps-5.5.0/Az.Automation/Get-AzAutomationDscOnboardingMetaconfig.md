---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 007142cb854e2e428983f95d7bb7397c5a0ace39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149410"
---
# <span data-ttu-id="2b308-101">Get-AzAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="2b308-101">Get-AzAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="2b308-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b308-102">SYNOPSIS</span></span>
<span data-ttu-id="2b308-103">Metakonfigurációs .mof fájlokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2b308-103">Creates meta-configuration .mof files.</span></span>

## <span data-ttu-id="2b308-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2b308-104">SYNTAX</span></span>

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b308-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2b308-105">DESCRIPTION</span></span>
<span data-ttu-id="2b308-106">A **Get-AzAutomationDscOnboardingMetaconfig** parancsmag létrehozza az APS–kívánt államkonfigurációs (DSC) metakonfigurációs Felügyelt objektumformátum (MOF) fájlokat.</span><span class="sxs-lookup"><span data-stu-id="2b308-106">The **Get-AzAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="2b308-107">Ez a parancsmag minden megadott számítógépnévhez létrehoz egy .mof fájlt.</span><span class="sxs-lookup"><span data-stu-id="2b308-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="2b308-108">A parancsmag létrehoz egy mappát az .mof fájlokhoz.</span><span class="sxs-lookup"><span data-stu-id="2b308-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="2b308-109">A mappához Set-DscLocalConfigurationManager parancsmag futtatásával DSC-csomópontokként használhatja ezeket a számítógépeket egy Azure Automation-fiókba.</span><span class="sxs-lookup"><span data-stu-id="2b308-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="2b308-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2b308-110">EXAMPLES</span></span>

### <span data-ttu-id="2b308-111">1. példa: Az Automatizálási DSC kiszolgálói</span><span class="sxs-lookup"><span data-stu-id="2b308-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="2b308-112">Az első parancs a Contoso17 nevű automatizálási fiók két kiszolgálójának DSC-metakonfigurációs fájljait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2b308-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="2b308-113">A parancs ezeket a fájlokat asztali gépre menti.</span><span class="sxs-lookup"><span data-stu-id="2b308-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="2b308-114">A második parancs a **Set-DscLocalConfigurationManager** parancsmag segítségével alkalmazza a metakonfigurációt a megadott számítógépekre, hogy DSC-csomópontokként használják őket.</span><span class="sxs-lookup"><span data-stu-id="2b308-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="2b308-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b308-115">PARAMETERS</span></span>

### <span data-ttu-id="2b308-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2b308-116">-AutomationAccountName</span></span>
<span data-ttu-id="2b308-117">Egy automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b308-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="2b308-118">A Számítógépnév paraméter által  megadott számítógépek be vannak adva a paraméterben megadott fiókba.</span><span class="sxs-lookup"><span data-stu-id="2b308-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="2b308-119">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="2b308-119">-ComputerName</span></span>
<span data-ttu-id="2b308-120">Azoknak a számítógépeknek a nevét tartalmazó tömböt adja meg, amelyekhez ez a parancsmag .mof fájlokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2b308-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="2b308-121">Ha nem adja meg ezt a paramétert, a parancsmag .mof fájlt hoz létre az aktuális számítógéphez (localhost).</span><span class="sxs-lookup"><span data-stu-id="2b308-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

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

### <span data-ttu-id="2b308-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b308-122">-DefaultProfile</span></span>
<span data-ttu-id="2b308-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2b308-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b308-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2b308-124">-Force</span></span>
<span data-ttu-id="2b308-125">A parancs futtatását kényszeríti anélkül, hogy megerősítést kérné, és lecserélné az azonos nevű meglévő .mof fájlokat.</span><span class="sxs-lookup"><span data-stu-id="2b308-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="2b308-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="2b308-126">-OutputFolder</span></span>
<span data-ttu-id="2b308-127">Annak a mappának a nevét adja meg, amelyben ez a parancsmag .mof fájlokat tárol.</span><span class="sxs-lookup"><span data-stu-id="2b308-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

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

### <span data-ttu-id="2b308-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b308-128">-ResourceGroupName</span></span>
<span data-ttu-id="2b308-129">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b308-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2b308-130">Ez a parancsmag .mof fájlokat hoz létre a számítógépére a paraméterként megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="2b308-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2b308-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b308-131">-Confirm</span></span>
<span data-ttu-id="2b308-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2b308-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b308-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b308-133">-WhatIf</span></span>
<span data-ttu-id="2b308-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2b308-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b308-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b308-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b308-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b308-136">CommonParameters</span></span>
<span data-ttu-id="2b308-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b308-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b308-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b308-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b308-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b308-139">INPUTS</span></span>

### <span data-ttu-id="2b308-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2b308-140">System.String</span></span>

### <span data-ttu-id="2b308-141">System.String[]</span><span class="sxs-lookup"><span data-stu-id="2b308-141">System.String[]</span></span>

## <span data-ttu-id="2b308-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b308-142">OUTPUTS</span></span>

### <span data-ttu-id="2b308-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="2b308-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="2b308-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2b308-144">NOTES</span></span>

## <span data-ttu-id="2b308-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b308-145">RELATED LINKS</span></span>
