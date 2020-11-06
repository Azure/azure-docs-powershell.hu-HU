---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f4d17fa6cdcb64aab2ab373420891f686facfdf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502260"
---
# <span data-ttu-id="aa2bc-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa2bc-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="aa2bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="aa2bc-103">Beolvassa az Azure automatizálási szoftverfrissítés konfigurációjának listáját.</span><span class="sxs-lookup"><span data-stu-id="aa2bc-103">Gets a list of azure automation software update configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa2bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa2bc-104">SYNTAX</span></span>

### <span data-ttu-id="aa2bc-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aa2bc-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa2bc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="aa2bc-106">ByName</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa2bc-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="aa2bc-107">ByVMId</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa2bc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa2bc-108">DESCRIPTION</span></span>
<span data-ttu-id="aa2bc-109">A Get-AzureRmAutomationSoftwareUpdateConfiguration a szoftverfrissítési konfigurációk listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="aa2bc-109">The Get-AzureRmAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="aa2bc-110">Ha egy bizonyos szoftverfrissítés-konfigurációt szeretne beszerezni, adja meg a Name (név) paramétert.</span><span class="sxs-lookup"><span data-stu-id="aa2bc-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="aa2bc-111">Azt is megteheti, hogy az Azure Resource id for this Virtual Machine rendszerhez megadhatja a szoftverfrissítési konfigurációkat, amelyek az Azure Virtual Machine-t célozzák meg.</span><span class="sxs-lookup"><span data-stu-id="aa2bc-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="aa2bc-112">Példák</span><span class="sxs-lookup"><span data-stu-id="aa2bc-112">EXAMPLES</span></span>

### <span data-ttu-id="aa2bc-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aa2bc-113">Example 1</span></span>
<span data-ttu-id="aa2bc-114">Az Azure automatizálási szoftverfrissítési konfigurációjának beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="aa2bc-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

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

## <span data-ttu-id="aa2bc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa2bc-115">PARAMETERS</span></span>

### <span data-ttu-id="aa2bc-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aa2bc-116">-AutomationAccountName</span></span>
<span data-ttu-id="aa2bc-117">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="aa2bc-117">The automation account name.</span></span>

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

### <span data-ttu-id="aa2bc-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="aa2bc-118">-AzureVMResourceId</span></span>
<span data-ttu-id="aa2bc-119">A virtuális gép Azure erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aa2bc-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="aa2bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa2bc-120">-DefaultProfile</span></span>
<span data-ttu-id="aa2bc-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa2bc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa2bc-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa2bc-122">-Name</span></span>
<span data-ttu-id="aa2bc-123">A szoftverfrissítési konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="aa2bc-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="aa2bc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa2bc-124">-ResourceGroupName</span></span>
<span data-ttu-id="aa2bc-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="aa2bc-125">The resource group name.</span></span>

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

### <span data-ttu-id="aa2bc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa2bc-126">CommonParameters</span></span>
<span data-ttu-id="aa2bc-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa2bc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa2bc-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa2bc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa2bc-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa2bc-129">INPUTS</span></span>

### <span data-ttu-id="aa2bc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="aa2bc-130">System.String</span></span>

## <span data-ttu-id="aa2bc-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa2bc-131">OUTPUTS</span></span>

### <span data-ttu-id="aa2bc-132">Microsoft. Azure. Command. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa2bc-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="aa2bc-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa2bc-133">NOTES</span></span>

## <span data-ttu-id="aa2bc-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa2bc-134">RELATED LINKS</span></span>
