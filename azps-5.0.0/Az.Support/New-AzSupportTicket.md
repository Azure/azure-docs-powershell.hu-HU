---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194166"
---
# <span data-ttu-id="27412-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="27412-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="27412-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27412-102">SYNOPSIS</span></span>
<span data-ttu-id="27412-103">Támogatási jegyet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="27412-103">Creates a support ticket.</span></span>

## <span data-ttu-id="27412-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27412-104">SYNTAX</span></span>

### <span data-ttu-id="27412-105">CreateSupportTicketWithContactDetailParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27412-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27412-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27412-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27412-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27412-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27412-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27412-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27412-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="27412-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27412-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="27412-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27412-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="27412-111">DESCRIPTION</span></span>
<span data-ttu-id="27412-112">Ezzel a parancsmaggal támogatási jegyet hozhat létre a számlázáshoz, az előfizetés-kezeléshez, a kvóta-vagy műszaki problémákhoz.</span><span class="sxs-lookup"><span data-stu-id="27412-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="27412-113">A Get-AzSupportService és az Get-AzSupportProblemClassification parancsmagok segítségével keresse meg az Azure-szolgáltatást, és a megfelelő probléma a probléma besorolása, amelyben támogatást szeretne kérni.</span><span class="sxs-lookup"><span data-stu-id="27412-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="27412-114">A következő paramétereket kell megadnia:</span><span class="sxs-lookup"><span data-stu-id="27412-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="27412-115">A New-AzSupportContactProfileObject-segéd parancsmag segítségével CustomerContactDetail-objektumokat hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="27412-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="27412-116">A felhőalapú megoldások szolgáltatói az ügyfél bérlői fiókjába bejelentkezve támogatási jegyet hozhatnak létre az ügyfél előfizetéséhez, és a *CSPHomeTenantId* paraméterrel megadhatják az otthoni bérlői azonosítót.</span><span class="sxs-lookup"><span data-stu-id="27412-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="27412-117">__Műszaki jegyek esetén:__</span><span class="sxs-lookup"><span data-stu-id="27412-117">__For technical tickets:__</span></span>

<span data-ttu-id="27412-118">Az erőforrás nevének megadásához adja meg az erőforrás ARM erőforrás-AZONOSÍTÓját a *TechnicalTicketResourceId* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="27412-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="27412-119">Lásd az alábbi példát.</span><span class="sxs-lookup"><span data-stu-id="27412-119">See an example below.</span></span> 

<span data-ttu-id="27412-120">__A kvóták esetében:__</span><span class="sxs-lookup"><span data-stu-id="27412-120">__For quota tickets:__</span></span>

<span data-ttu-id="27412-121">Ha a **VM-magok** , a **köteg** , az SQL- **adatbázis** és az **SQL-adattárház** kvótájának növelését szeretné kérni, további részleteket adhat meg a *QuotaTicketDetail* objektum csoportban.</span><span class="sxs-lookup"><span data-stu-id="27412-121">To request for quota increase for **Compute VM Cores** , **Batch** , **SQL Database** and **SQL Data Warehouse** , provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="27412-122">Az QuotaTicketDetail objektum 3 tulajdonságból áll, az alább leírt módon.</span><span class="sxs-lookup"><span data-stu-id="27412-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="27412-123">Részletes dokumentációért [kattintson ide.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="27412-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="27412-124">Ha részletesen szeretné tudni, hogy miként építhet fel hasznos tartalmakat a különféle kontingensek típusaira, [kattintson ide](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="27412-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="27412-125">Példák</span><span class="sxs-lookup"><span data-stu-id="27412-125">EXAMPLES</span></span>

### <span data-ttu-id="27412-126">Példa 1: számlázási vagy előfizetés-kezelési támogatási jegy létrehozása.</span><span class="sxs-lookup"><span data-stu-id="27412-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="27412-127">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a számlázási vagy az előfizetés-kezelési problémák helyes AZONOSÍTÓját, amelyre támogatást szeretne kérni</span><span class="sxs-lookup"><span data-stu-id="27412-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-128">2. példa: terméktámogatási jegy létrehozása a virtuális gép Windows-erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="27412-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="27412-129">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a Windows-alapú virtuális gép megfelelő GUID-azonosítóit, amelyekre támogatást szeretne kérni</span><span class="sxs-lookup"><span data-stu-id="27412-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-130">3. példa: kvóta-támogatási jegy létrehozása egy adott VM-családhoz tartozó virtuális gép magok kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="27412-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="27412-131">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével a kvóta kiszámításához a VM magok probléma besorolása című fejezet helyes GUID-elemeit olvashatja be.</span><span class="sxs-lookup"><span data-stu-id="27412-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-132">Példa 4: kvóta-támogatási jegy létrehozása egy köteg-fiókban a kis prioritású magok kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="27412-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="27412-133">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta-használati problémák besorolásának megfelelő GUID-elemeit.</span><span class="sxs-lookup"><span data-stu-id="27412-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-134">Példa 5: kvóta-támogatási jegy létrehozása egy adott VM-családhoz tartozó VM magok kvótájának növelése céljából egy köteg fiók esetén.</span><span class="sxs-lookup"><span data-stu-id="27412-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="27412-135">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta-használati problémák besorolásának megfelelő GUID-elemeit.</span><span class="sxs-lookup"><span data-stu-id="27412-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-136">6. példa: kvóta-támogatási jegy létrehozása egy köteghez tartozó készlet kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="27412-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="27412-137">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta-használati problémák besorolásának megfelelő GUID-elemeit.</span><span class="sxs-lookup"><span data-stu-id="27412-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-138">7. példa: kvóta-támogatási jegy létrehozása a kötegelt fiók aktív feladatainak és munkaütemezések kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="27412-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="27412-139">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta-használati problémák besorolásának megfelelő GUID-elemeit.</span><span class="sxs-lookup"><span data-stu-id="27412-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-140">8. példa: kvóta-támogatási jegy létrehozása az előfizetéshez tartozó kötegelt fiókok számának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="27412-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="27412-141">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta-használati problémák besorolásának megfelelő GUID-elemeit.</span><span class="sxs-lookup"><span data-stu-id="27412-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-142">9. példa: kvóta-támogatási jegy létrehozása az SQL-adatbázis DTU kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="27412-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="27412-143">Az Get-AzSupportService és a Get-AzSupportProblemClassification segítségével beolvashatja a kvóta SQL-adatbázis problémáinak besorolása című fejezet helyes GUID azonosítóit.</span><span class="sxs-lookup"><span data-stu-id="27412-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-144">10. példa: kvóta-támogatási jegy létrehozása az SQL-adatbázis kiszolgálói kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="27412-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="27412-145">Az Get-AzSupportService és a Get-AzSupportProblemClassification segítségével beolvashatja a kvóta SQL-adatbázis problémáinak besorolása című fejezet helyes GUID azonosítóit.</span><span class="sxs-lookup"><span data-stu-id="27412-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-146">11-es példa: kvóta-támogatási jegy létrehozása az SQL-adattárház DTU kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="27412-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="27412-147">Az Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta SQL Date Warehouse-probléma besorolásának megfelelő GUID-azonosítókat.</span><span class="sxs-lookup"><span data-stu-id="27412-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-148">12 példa: kvóta-támogatási jegy létrehozása az SQL-adattárházban lévő kiszolgálók kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="27412-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="27412-149">A kvóta SQL-adatraktár problémáinak osztályozása az Get-AzSupportService és a Get-AzSupportProblemClassification használatával.</span><span class="sxs-lookup"><span data-stu-id="27412-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-150">13. példa: kvóta-támogatási jegy létrehozása a kis prioritású magokra vonatkozó kvóta növeléséhez a gépi tanulási szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="27412-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="27412-151">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta-automaták tanulási szolgáltatási problémájának megfelelő GUID-azonosítókat.</span><span class="sxs-lookup"><span data-stu-id="27412-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-152">14. példa: kvóta-támogatási jegy létrehozása a VM magok kvótájának növelése egy adott VM-családban a gépi tanulási szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="27412-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="27412-153">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta-automaták tanulási szolgáltatási problémájának megfelelő GUID-azonosítókat.</span><span class="sxs-lookup"><span data-stu-id="27412-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-154">15. példa: kvóta-támogatási jegy létrehozása az Azure SQL-alapú felügyelt példány kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="27412-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="27412-155">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta SQL-alapú felügyelt példány-kezelési problémájának megfelelő GUID-azonosítókat.</span><span class="sxs-lookup"><span data-stu-id="27412-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-156">16 példa: támogatási jegy létrehozása a CustomerContactDetail objektum helyett az egyes ügyfél-kapcsolatfelvételi paraméterek megadásával.</span><span class="sxs-lookup"><span data-stu-id="27412-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-157">17. példa: támogatási jegy létrehozása az Azure 24 x 7 válaszára vonatkozó kéréssel</span><span class="sxs-lookup"><span data-stu-id="27412-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="27412-158">18. példa: a támogatási jegy létrehozása az ügyfél nevében a felhőalapú megoldás-szolgáltató (CSP) esetén.</span><span class="sxs-lookup"><span data-stu-id="27412-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="27412-159">A CSP-nek először be kell jelentkeznie a bérlői webhelyre, majd be kell jelentkeznie az ügyfél bérlői webhelyére az alábbi példa szerint.</span><span class="sxs-lookup"><span data-stu-id="27412-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="27412-160">A támogatási jegy létrehozásakor a-CSPHomeTenantId paraméterrel meg kell adnia az otthoni bérlői azonosítót.</span><span class="sxs-lookup"><span data-stu-id="27412-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="27412-161">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27412-161">PARAMETERS</span></span>

### <span data-ttu-id="27412-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="27412-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="27412-163">További e-mail-címek.</span><span class="sxs-lookup"><span data-stu-id="27412-163">Additional email addresses.</span></span>
<span data-ttu-id="27412-164">Az itt felsorolt e-mail-címeket a támogatási jegyre vonatkozó minden levelezésre másolhatja.</span><span class="sxs-lookup"><span data-stu-id="27412-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27412-165">-AsJob</span></span>
<span data-ttu-id="27412-166">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="27412-166">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="27412-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="27412-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="27412-168">Ez a felhőalapú megoldás-szolgáltató felhasználó otthoni bérlői azonosítója, amellyel támogatási jegyet hozhat létre az ügyfél számára.</span><span class="sxs-lookup"><span data-stu-id="27412-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="27412-169">-CustomerContactDetail</span></span>
<span data-ttu-id="27412-170">Az SupportTicket-erőforráshoz társított ügyfél-elérhetőségi adatok.</span><span class="sxs-lookup"><span data-stu-id="27412-170">Customer contact details associated with SupportTicket resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: CreateSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="27412-171">-CustomerCountry</span></span>
<span data-ttu-id="27412-172">Ügyfél országa.</span><span class="sxs-lookup"><span data-stu-id="27412-172">Customer country.</span></span>
<span data-ttu-id="27412-173">A kódnak érvényes ISO Alpha-3 országkód (ISO 3166) kell lennie.</span><span class="sxs-lookup"><span data-stu-id="27412-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="27412-174">-CustomerFirstName</span></span>
<span data-ttu-id="27412-175">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="27412-175">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="27412-176">-CustomerLastName</span></span>
<span data-ttu-id="27412-177">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="27412-177">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="27412-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="27412-179">Ügyfél telefonszáma.</span><span class="sxs-lookup"><span data-stu-id="27412-179">Customer phone number.</span></span>
<span data-ttu-id="27412-180">Erre akkor van szükség, ha az elsődleges névjegykártya-módszer telefon.</span><span class="sxs-lookup"><span data-stu-id="27412-180">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="27412-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="27412-182">Az egyéni Peferred nyelve.</span><span class="sxs-lookup"><span data-stu-id="27412-182">Peferred language of the custom.</span></span>
<span data-ttu-id="27412-183">Ennek az itt felsorolt támogatott nyelvek egyikéhez érvényes célnyelv-kódnak kell lennie https://azure.microsoft.com/en-us/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="27412-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="27412-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="27412-185">Ügyfél által preferált időzóna</span><span class="sxs-lookup"><span data-stu-id="27412-185">Customer preferred time zone.</span></span>
<span data-ttu-id="27412-186">Ennek érvényes System.TimeZoneInfo.Id-értéknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="27412-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="27412-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="27412-188">Ügyfél elsődleges e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="27412-188">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27412-189">-DefaultProfile</span></span>
<span data-ttu-id="27412-190">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27412-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27412-191">-Leírás</span><span class="sxs-lookup"><span data-stu-id="27412-191">-Description</span></span>
<span data-ttu-id="27412-192">A kérdés vagy probléma részletes leírása.</span><span class="sxs-lookup"><span data-stu-id="27412-192">Detailed description of the question or issue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-193">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27412-193">-Name</span></span>
<span data-ttu-id="27412-194">A parancsmag által létrehozott támogatási jegy neve.</span><span class="sxs-lookup"><span data-stu-id="27412-194">Name of support ticket that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="27412-195">-PreferredContactMethod</span></span>
<span data-ttu-id="27412-196">Preferált kontakt mód</span><span class="sxs-lookup"><span data-stu-id="27412-196">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="27412-197">-ProblemClassificationId</span></span>
<span data-ttu-id="27412-198">Minden Azure-szolgáltatáshoz tartozik egy saját, a problémára vonatkozó besorolási kategória, amely megfelel az észlelt probléma típusának.</span><span class="sxs-lookup"><span data-stu-id="27412-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="27412-199">Ez a paraméter a ProblemClassification-erőforrás ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="27412-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="27412-200">-ProblemStartTime</span></span>
<span data-ttu-id="27412-201">A probléma kezdetének dátuma és időpontja.</span><span class="sxs-lookup"><span data-stu-id="27412-201">Date and time when the problem started.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="27412-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="27412-203">További részletek a kvóta-támogatási jegyekről.</span><span class="sxs-lookup"><span data-stu-id="27412-203">Additional details for a Quota support ticket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSQuotaTicketDetail
Parameter Sets: CreateQuotaSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="27412-204">-Require24X7Response</span></span>
<span data-ttu-id="27412-205">Jelzi, hogy ez a támogatási jegy az Azuretól kapott 24x7 választ igényli-e.</span><span class="sxs-lookup"><span data-stu-id="27412-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

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

### <span data-ttu-id="27412-206">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="27412-206">-Severity</span></span>
<span data-ttu-id="27412-207">A támogatási jegy súlyossága.</span><span class="sxs-lookup"><span data-stu-id="27412-207">Severity of the support ticket.</span></span>
<span data-ttu-id="27412-208">Ez jelzi az eset sürgősségét, ami viszont az Azure-szal kötött technikai támogatási csomag szolgáltatási szintről szóló szerződése szerint a válaszadás időpontját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="27412-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="27412-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="27412-210">Ez az Azure szolgáltatási erőforrás erőforrás-azonosítója (például: egy virtuális gép vagy egy HDInsight-erőforrás), amelyhez a támogatási jegyet létrehozta.</span><span class="sxs-lookup"><span data-stu-id="27412-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-211">-Cím</span><span class="sxs-lookup"><span data-stu-id="27412-211">-Title</span></span>
<span data-ttu-id="27412-212">A támogatási jegy címe.</span><span class="sxs-lookup"><span data-stu-id="27412-212">Title of support ticket.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27412-213">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27412-213">-Confirm</span></span>
<span data-ttu-id="27412-214">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27412-214">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27412-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27412-215">-WhatIf</span></span>
<span data-ttu-id="27412-216">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27412-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27412-217">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27412-217">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27412-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27412-218">CommonParameters</span></span>
<span data-ttu-id="27412-219">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27412-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27412-220">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="27412-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27412-221">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27412-221">INPUTS</span></span>

### <span data-ttu-id="27412-222">Nincs</span><span class="sxs-lookup"><span data-stu-id="27412-222">None</span></span>

## <span data-ttu-id="27412-223">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27412-223">OUTPUTS</span></span>

### <span data-ttu-id="27412-224">Microsoft. Azure. commands. support. models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="27412-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="27412-225">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27412-225">NOTES</span></span>

## <span data-ttu-id="27412-226">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27412-226">RELATED LINKS</span></span>
