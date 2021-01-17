---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478681"
---
# <span data-ttu-id="17c3e-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="17c3e-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="17c3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="17c3e-103">Lekérte az Azure Automatizálási szoftverfrissítések konfigurációjának listáját.</span><span class="sxs-lookup"><span data-stu-id="17c3e-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="17c3e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="17c3e-104">SYNTAX</span></span>

### <span data-ttu-id="17c3e-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="17c3e-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17c3e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="17c3e-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17c3e-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="17c3e-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17c3e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="17c3e-108">DESCRIPTION</span></span>
<span data-ttu-id="17c3e-109">A Get-AzAutomationSoftwareUpdateConfiguration a szoftverfrissítések konfigurációjának listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="17c3e-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="17c3e-110">Adott szoftverfrissítés-konfiguráció megadásához adja meg a név paraméterét.</span><span class="sxs-lookup"><span data-stu-id="17c3e-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="17c3e-111">A virtuális gép azure-erőforrás-azonosítójának megadásával listába is sorolhatja az egyes Azure virtuális gépekre vonatkozó szoftverfrissítés-konfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="17c3e-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="17c3e-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="17c3e-112">EXAMPLES</span></span>

### <span data-ttu-id="17c3e-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="17c3e-113">Example 1</span></span>
<span data-ttu-id="17c3e-114">Azure Automatizálási szoftverfrissítések név szerint való konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="17c3e-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Succeeded
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:37 AM +00:00
Description           :
```

## <span data-ttu-id="17c3e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17c3e-115">PARAMETERS</span></span>

### <span data-ttu-id="17c3e-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="17c3e-116">-AutomationAccountName</span></span>
<span data-ttu-id="17c3e-117">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="17c3e-117">The automation account name.</span></span>

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

### <span data-ttu-id="17c3e-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="17c3e-118">-AzureVMResourceId</span></span>
<span data-ttu-id="17c3e-119">A virtuális gép Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="17c3e-119">Azure resource Id of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVMId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17c3e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17c3e-120">-DefaultProfile</span></span>
<span data-ttu-id="17c3e-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17c3e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17c3e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="17c3e-122">-Name</span></span>
<span data-ttu-id="17c3e-123">A szoftverfrissítés-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="17c3e-123">Name of the software update configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17c3e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17c3e-124">-ResourceGroupName</span></span>
<span data-ttu-id="17c3e-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="17c3e-125">The resource group name.</span></span>

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

### <span data-ttu-id="17c3e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c3e-126">CommonParameters</span></span>
<span data-ttu-id="17c3e-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17c3e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c3e-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17c3e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c3e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17c3e-129">INPUTS</span></span>

### <span data-ttu-id="17c3e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="17c3e-130">System.String</span></span>

## <span data-ttu-id="17c3e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17c3e-131">OUTPUTS</span></span>

### <span data-ttu-id="17c3e-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="17c3e-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="17c3e-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="17c3e-133">NOTES</span></span>

## <span data-ttu-id="17c3e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17c3e-134">RELATED LINKS</span></span>
