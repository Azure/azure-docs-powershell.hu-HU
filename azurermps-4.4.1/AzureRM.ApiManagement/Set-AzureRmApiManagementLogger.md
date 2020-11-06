---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: c21c227dd748f28523f4ac616d003e029d19e38f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499276"
---
# <span data-ttu-id="9a14d-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="9a14d-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="9a14d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a14d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a14d-103">API-kezelési naplózó módosítása</span><span class="sxs-lookup"><span data-stu-id="9a14d-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a14d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a14d-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a14d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a14d-105">DESCRIPTION</span></span>
<span data-ttu-id="9a14d-106">A **set-AzureRmApiManagementLogger** parancsmag módosította az Azure API-kezelési **naplózó** beállításait.</span><span class="sxs-lookup"><span data-stu-id="9a14d-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="9a14d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9a14d-107">EXAMPLES</span></span>

### <span data-ttu-id="9a14d-108">Példa 1: naplózó módosítása</span><span class="sxs-lookup"><span data-stu-id="9a14d-108">Example 1: Modify a logger</span></span>
```
PS C:\>Set-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="9a14d-109">Ez a parancs módosítja az id Logger123 tartalmazó naplózó.</span><span class="sxs-lookup"><span data-stu-id="9a14d-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="9a14d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a14d-110">PARAMETERS</span></span>

### <span data-ttu-id="9a14d-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="9a14d-111">-ConnectionString</span></span>
<span data-ttu-id="9a14d-112">Egy Azure-esemény hubok kapcsolati karakterláncát adja meg, amely a házirend-jogosultságok küldését is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9a14d-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="9a14d-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9a14d-113">-Context</span></span>
<span data-ttu-id="9a14d-114">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9a14d-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a14d-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9a14d-115">-Description</span></span>
<span data-ttu-id="9a14d-116">Leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="9a14d-116">Specifies a description.</span></span>

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

### <span data-ttu-id="9a14d-117">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="9a14d-117">-IsBuffered</span></span>
<span data-ttu-id="9a14d-118">Azt adja meg, hogy a naplózó rekordjai a közzététel előtt puffereltek.</span><span class="sxs-lookup"><span data-stu-id="9a14d-118">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="9a14d-119">Ha a rekordokat pufferelte, akkor a rendszer 15 másodpercenként elküldi az esemény-huboknak, vagy ha a puffer az 256 KB-ot kapja.</span><span class="sxs-lookup"><span data-stu-id="9a14d-119">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="9a14d-120">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="9a14d-120">-LoggerId</span></span>
<span data-ttu-id="9a14d-121">A frissítendő naplózó AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a14d-121">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="9a14d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9a14d-122">-Name</span></span>
<span data-ttu-id="9a14d-123">Az Azure Classic portálról adja meg az esemény központja egyedének nevét.</span><span class="sxs-lookup"><span data-stu-id="9a14d-123">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="9a14d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a14d-124">-PassThru</span></span>
<span data-ttu-id="9a14d-125">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementLogger** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9a14d-125">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9a14d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a14d-126">-DefaultProfile</span></span>
<span data-ttu-id="9a14d-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a14d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a14d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a14d-128">CommonParameters</span></span>
<span data-ttu-id="9a14d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a14d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a14d-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a14d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a14d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a14d-131">INPUTS</span></span>

## <span data-ttu-id="9a14d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a14d-132">OUTPUTS</span></span>

### <span data-ttu-id="9a14d-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="9a14d-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="9a14d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a14d-134">NOTES</span></span>

## <span data-ttu-id="9a14d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a14d-135">RELATED LINKS</span></span>

[<span data-ttu-id="9a14d-136">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="9a14d-136">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="9a14d-137">Új – AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="9a14d-137">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="9a14d-138">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="9a14d-138">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


