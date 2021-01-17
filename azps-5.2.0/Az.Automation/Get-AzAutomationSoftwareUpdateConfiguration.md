---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373728"
---
# <span data-ttu-id="5797b-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="5797b-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="5797b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5797b-102">SYNOPSIS</span></span>
<span data-ttu-id="5797b-103">Az Azure Automatizálási szoftverfrissítések konfigurációjának listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5797b-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="5797b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5797b-104">SYNTAX</span></span>

### <span data-ttu-id="5797b-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5797b-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5797b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5797b-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5797b-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="5797b-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5797b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5797b-108">DESCRIPTION</span></span>
<span data-ttu-id="5797b-109">A Get-AzAutomationSoftwareUpdateConfiguration a szoftverfrissítések konfigurációjának listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="5797b-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="5797b-110">Adott szoftverfrissítés-konfiguráció megadásához adja meg a név paraméterét.</span><span class="sxs-lookup"><span data-stu-id="5797b-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="5797b-111">A virtuális gép azure-erőforrás-azonosítójának megadásával listába is sorolhatja az egyes Azure virtuális gépekre vonatkozó szoftverfrissítés-konfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="5797b-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="5797b-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5797b-112">EXAMPLES</span></span>

### <span data-ttu-id="5797b-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="5797b-113">Example 1</span></span>
<span data-ttu-id="5797b-114">Azure Automation-szoftverfrissítések név szerint való beállítása.</span><span class="sxs-lookup"><span data-stu-id="5797b-114">Get an azure automation software update configuration by name.</span></span>

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

## <span data-ttu-id="5797b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5797b-115">PARAMETERS</span></span>

### <span data-ttu-id="5797b-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5797b-116">-AutomationAccountName</span></span>
<span data-ttu-id="5797b-117">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="5797b-117">The automation account name.</span></span>

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

### <span data-ttu-id="5797b-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="5797b-118">-AzureVMResourceId</span></span>
<span data-ttu-id="5797b-119">A virtuális gép Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="5797b-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="5797b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5797b-120">-DefaultProfile</span></span>
<span data-ttu-id="5797b-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5797b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5797b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5797b-122">-Name</span></span>
<span data-ttu-id="5797b-123">A szoftverfrissítés-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="5797b-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="5797b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5797b-124">-ResourceGroupName</span></span>
<span data-ttu-id="5797b-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5797b-125">The resource group name.</span></span>

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

### <span data-ttu-id="5797b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5797b-126">CommonParameters</span></span>
<span data-ttu-id="5797b-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5797b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5797b-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5797b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5797b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5797b-129">INPUTS</span></span>

### <span data-ttu-id="5797b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5797b-130">System.String</span></span>

## <span data-ttu-id="5797b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5797b-131">OUTPUTS</span></span>

### <span data-ttu-id="5797b-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="5797b-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="5797b-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5797b-133">NOTES</span></span>

## <span data-ttu-id="5797b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5797b-134">RELATED LINKS</span></span>
