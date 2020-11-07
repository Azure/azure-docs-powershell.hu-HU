---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 8f1931cb5e73e3850cd011c16d327f8e8abc3a47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667934"
---
# <span data-ttu-id="43a10-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="43a10-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="43a10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43a10-102">SYNOPSIS</span></span>
<span data-ttu-id="43a10-103">API-kezelési naplózó módosítása</span><span class="sxs-lookup"><span data-stu-id="43a10-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="43a10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43a10-104">SYNTAX</span></span>

### <span data-ttu-id="43a10-105">EventHubLoggerSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43a10-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43a10-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="43a10-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43a10-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="43a10-107">DESCRIPTION</span></span>
<span data-ttu-id="43a10-108">A **set-AzApiManagementLogger** parancsmag módosította az Azure API-kezelési **naplózó** beállításait.</span><span class="sxs-lookup"><span data-stu-id="43a10-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="43a10-109">Példák</span><span class="sxs-lookup"><span data-stu-id="43a10-109">EXAMPLES</span></span>

### <span data-ttu-id="43a10-110">Példa 1: a EventHub Logger módosítása</span><span class="sxs-lookup"><span data-stu-id="43a10-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="43a10-111">Ez a parancs módosítja az id Logger123 tartalmazó naplózó.</span><span class="sxs-lookup"><span data-stu-id="43a10-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="43a10-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43a10-112">PARAMETERS</span></span>

### <span data-ttu-id="43a10-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="43a10-113">-ConnectionString</span></span>
<span data-ttu-id="43a10-114">Egy Azure-esemény hubok kapcsolati karakterláncát adja meg, amely a házirend-jogosultságok küldését is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="43a10-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a10-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="43a10-115">-Context</span></span>
<span data-ttu-id="43a10-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="43a10-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43a10-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a10-117">-DefaultProfile</span></span>
<span data-ttu-id="43a10-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43a10-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43a10-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="43a10-119">-Description</span></span>
<span data-ttu-id="43a10-120">Leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="43a10-120">Specifies a description.</span></span>

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

### <span data-ttu-id="43a10-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="43a10-121">-InstrumentationKey</span></span>
<span data-ttu-id="43a10-122">Az alkalmazási áttekintések Instrumentation kulcsa.</span><span class="sxs-lookup"><span data-stu-id="43a10-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="43a10-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="43a10-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a10-124">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="43a10-124">-IsBuffered</span></span>
<span data-ttu-id="43a10-125">Azt adja meg, hogy a naplózó rekordjai a közzététel előtt puffereltek.</span><span class="sxs-lookup"><span data-stu-id="43a10-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="43a10-126">Ha a rekordokat pufferelte, akkor a rendszer 15 másodpercenként elküldi az esemény-huboknak, vagy ha a puffer az 256 KB-ot kapja.</span><span class="sxs-lookup"><span data-stu-id="43a10-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a10-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="43a10-127">-LoggerId</span></span>
<span data-ttu-id="43a10-128">A frissítendő naplózó AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="43a10-128">Specifies the ID of the logger to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a10-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43a10-129">-Name</span></span>
<span data-ttu-id="43a10-130">Az Azure Classic portálról adja meg az esemény központja egyedének nevét.</span><span class="sxs-lookup"><span data-stu-id="43a10-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a10-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43a10-131">-PassThru</span></span>
<span data-ttu-id="43a10-132">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementLogger** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="43a10-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a10-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43a10-133">-Confirm</span></span>
<span data-ttu-id="43a10-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43a10-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43a10-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43a10-135">-WhatIf</span></span>
<span data-ttu-id="43a10-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43a10-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43a10-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43a10-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43a10-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a10-138">CommonParameters</span></span>
<span data-ttu-id="43a10-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43a10-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a10-140">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="43a10-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a10-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43a10-141">INPUTS</span></span>

### <span data-ttu-id="43a10-142">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="43a10-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="43a10-143">System. String</span><span class="sxs-lookup"><span data-stu-id="43a10-143">System.String</span></span>

### <span data-ttu-id="43a10-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="43a10-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="43a10-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43a10-145">OUTPUTS</span></span>

### <span data-ttu-id="43a10-146">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="43a10-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="43a10-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43a10-147">NOTES</span></span>

## <span data-ttu-id="43a10-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43a10-148">RELATED LINKS</span></span>

[<span data-ttu-id="43a10-149">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="43a10-149">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="43a10-150">Új – AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="43a10-150">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="43a10-151">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="43a10-151">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)


