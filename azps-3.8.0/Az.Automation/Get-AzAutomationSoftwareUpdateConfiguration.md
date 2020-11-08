---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012662"
---
# <span data-ttu-id="517b8-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="517b8-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="517b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="517b8-102">SYNOPSIS</span></span>
<span data-ttu-id="517b8-103">Beolvassa az Azure automatizálási szoftverfrissítés konfigurációjának listáját.</span><span class="sxs-lookup"><span data-stu-id="517b8-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="517b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="517b8-104">SYNTAX</span></span>

### <span data-ttu-id="517b8-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="517b8-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="517b8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="517b8-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="517b8-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="517b8-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="517b8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="517b8-108">DESCRIPTION</span></span>
<span data-ttu-id="517b8-109">A Get-AzAutomationSoftwareUpdateConfiguration a szoftverfrissítési konfigurációk listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="517b8-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="517b8-110">Ha egy bizonyos szoftverfrissítés-konfigurációt szeretne beszerezni, adja meg a Name (név) paramétert.</span><span class="sxs-lookup"><span data-stu-id="517b8-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="517b8-111">Azt is megteheti, hogy az Azure Resource id for this Virtual Machine rendszerhez megadhatja a szoftverfrissítési konfigurációkat, amelyek az Azure Virtual Machine-t célozzák meg.</span><span class="sxs-lookup"><span data-stu-id="517b8-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="517b8-112">Példák</span><span class="sxs-lookup"><span data-stu-id="517b8-112">EXAMPLES</span></span>

### <span data-ttu-id="517b8-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="517b8-113">Example 1</span></span>
<span data-ttu-id="517b8-114">Az Azure automatizálási szoftverfrissítési konfigurációjának beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="517b8-114">Get an azure automation software update configuration by name.</span></span>

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

## <span data-ttu-id="517b8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="517b8-115">PARAMETERS</span></span>

### <span data-ttu-id="517b8-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="517b8-116">-AutomationAccountName</span></span>
<span data-ttu-id="517b8-117">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="517b8-117">The automation account name.</span></span>

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

### <span data-ttu-id="517b8-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="517b8-118">-AzureVMResourceId</span></span>
<span data-ttu-id="517b8-119">A virtuális gép Azure erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="517b8-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="517b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="517b8-120">-DefaultProfile</span></span>
<span data-ttu-id="517b8-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="517b8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="517b8-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="517b8-122">-Name</span></span>
<span data-ttu-id="517b8-123">A szoftverfrissítési konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="517b8-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="517b8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="517b8-124">-ResourceGroupName</span></span>
<span data-ttu-id="517b8-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="517b8-125">The resource group name.</span></span>

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

### <span data-ttu-id="517b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="517b8-126">CommonParameters</span></span>
<span data-ttu-id="517b8-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="517b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="517b8-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="517b8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="517b8-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="517b8-129">INPUTS</span></span>

### <span data-ttu-id="517b8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="517b8-130">System.String</span></span>

## <span data-ttu-id="517b8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="517b8-131">OUTPUTS</span></span>

### <span data-ttu-id="517b8-132">Microsoft. Azure. Command. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="517b8-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="517b8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="517b8-133">NOTES</span></span>

## <span data-ttu-id="517b8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="517b8-134">RELATED LINKS</span></span>
