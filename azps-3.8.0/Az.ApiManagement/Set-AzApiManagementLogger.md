---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 6ad32b3bd9bef4f4e684125b280db941da7a7b3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014180"
---
# <span data-ttu-id="73c59-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="73c59-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="73c59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73c59-102">SYNOPSIS</span></span>
<span data-ttu-id="73c59-103">API-kezelési naplózó módosítása</span><span class="sxs-lookup"><span data-stu-id="73c59-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="73c59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73c59-104">SYNTAX</span></span>

### <span data-ttu-id="73c59-105">EventHubLoggerSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="73c59-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73c59-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="73c59-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73c59-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="73c59-107">DESCRIPTION</span></span>
<span data-ttu-id="73c59-108">A **set-AzApiManagementLogger** parancsmag módosította az Azure API-kezelési **naplózó** beállításait.</span><span class="sxs-lookup"><span data-stu-id="73c59-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="73c59-109">Példák</span><span class="sxs-lookup"><span data-stu-id="73c59-109">EXAMPLES</span></span>

### <span data-ttu-id="73c59-110">Példa 1: a EventHub Logger módosítása</span><span class="sxs-lookup"><span data-stu-id="73c59-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="73c59-111">Ez a parancs módosítja az id Logger123 tartalmazó naplózó.</span><span class="sxs-lookup"><span data-stu-id="73c59-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="73c59-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73c59-112">PARAMETERS</span></span>

### <span data-ttu-id="73c59-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="73c59-113">-ConnectionString</span></span>
<span data-ttu-id="73c59-114">Egy Azure-esemény hubok kapcsolati karakterláncát adja meg, amely a házirend-jogosultságok küldését is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="73c59-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="73c59-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="73c59-115">-Context</span></span>
<span data-ttu-id="73c59-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="73c59-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="73c59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c59-117">-DefaultProfile</span></span>
<span data-ttu-id="73c59-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73c59-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73c59-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="73c59-119">-Description</span></span>
<span data-ttu-id="73c59-120">Leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="73c59-120">Specifies a description.</span></span>

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

### <span data-ttu-id="73c59-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="73c59-121">-InstrumentationKey</span></span>
<span data-ttu-id="73c59-122">Az alkalmazási áttekintések Instrumentation kulcsa.</span><span class="sxs-lookup"><span data-stu-id="73c59-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="73c59-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="73c59-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="73c59-124">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="73c59-124">-IsBuffered</span></span>
<span data-ttu-id="73c59-125">Azt adja meg, hogy a naplózó rekordjai a közzététel előtt puffereltek.</span><span class="sxs-lookup"><span data-stu-id="73c59-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="73c59-126">Ha a rekordokat pufferelte, akkor a rendszer 15 másodpercenként elküldi az esemény-huboknak, vagy ha a puffer az 256 KB-ot kapja.</span><span class="sxs-lookup"><span data-stu-id="73c59-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="73c59-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="73c59-127">-LoggerId</span></span>
<span data-ttu-id="73c59-128">A frissítendő naplózó AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="73c59-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="73c59-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="73c59-129">-Name</span></span>
<span data-ttu-id="73c59-130">Az Azure Classic portálról adja meg az esemény központja egyedének nevét.</span><span class="sxs-lookup"><span data-stu-id="73c59-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="73c59-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73c59-131">-PassThru</span></span>
<span data-ttu-id="73c59-132">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementLogger** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="73c59-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="73c59-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="73c59-133">-Confirm</span></span>
<span data-ttu-id="73c59-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="73c59-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73c59-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73c59-135">-WhatIf</span></span>
<span data-ttu-id="73c59-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="73c59-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73c59-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73c59-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73c59-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c59-138">CommonParameters</span></span>
<span data-ttu-id="73c59-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73c59-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c59-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="73c59-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c59-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73c59-141">INPUTS</span></span>

### <span data-ttu-id="73c59-142">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="73c59-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="73c59-143">System. String</span><span class="sxs-lookup"><span data-stu-id="73c59-143">System.String</span></span>

### <span data-ttu-id="73c59-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="73c59-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="73c59-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73c59-145">OUTPUTS</span></span>

### <span data-ttu-id="73c59-146">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="73c59-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="73c59-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73c59-147">NOTES</span></span>

## <span data-ttu-id="73c59-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73c59-148">RELATED LINKS</span></span>

[<span data-ttu-id="73c59-149">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="73c59-149">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="73c59-150">Új – AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="73c59-150">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="73c59-151">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="73c59-151">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)


