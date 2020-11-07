---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: dc3beb041a143ed151c19e0623f5db7f5f6d61e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847478"
---
# <span data-ttu-id="036c6-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="036c6-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="036c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="036c6-102">SYNOPSIS</span></span>
<span data-ttu-id="036c6-103">Támogatási jegyet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="036c6-103">Creates a support ticket.</span></span>

## <span data-ttu-id="036c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="036c6-104">SYNTAX</span></span>

### <span data-ttu-id="036c6-105">CreateSupportTicketWithContactDetailParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="036c6-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="036c6-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="036c6-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="036c6-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="036c6-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="036c6-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="036c6-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="036c6-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="036c6-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="036c6-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="036c6-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="036c6-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="036c6-111">DESCRIPTION</span></span>
<span data-ttu-id="036c6-112">Ezzel a parancsmaggal támogatási jegyet hozhat létre a számlázáshoz, az előfizetés-kezeléshez, a kvóta-vagy műszaki problémákhoz.</span><span class="sxs-lookup"><span data-stu-id="036c6-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="036c6-113">A Get-AzSupportService és az Get-AzSupportProblemClassification parancsmagok segítségével keresse meg az Azure-szolgáltatást, és a megfelelő probléma a probléma besorolása, amelyben támogatást szeretne kérni.</span><span class="sxs-lookup"><span data-stu-id="036c6-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="036c6-114">A következő paramétereket kell megadnia:</span><span class="sxs-lookup"><span data-stu-id="036c6-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="036c6-115">A New-AzSupportContactProfileObject-segéd parancsmag segítségével CustomerContactDetail-objektumokat hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="036c6-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="036c6-116">A felhőalapú megoldások szolgáltatói az ügyfél bérlői fiókjába bejelentkezve támogatási jegyet hozhatnak létre az ügyfél előfizetéséhez, és a *CSPHomeTenantId* paraméterrel megadhatják az otthoni bérlői azonosítót.</span><span class="sxs-lookup"><span data-stu-id="036c6-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="036c6-117">__Műszaki jegyek esetén:__</span><span class="sxs-lookup"><span data-stu-id="036c6-117">__For technical tickets:__</span></span>

<span data-ttu-id="036c6-118">Az erőforrás nevének megadásához adja meg az erőforrás ARM erőforrás-AZONOSÍTÓját a *TechnicalTicketResourceId* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="036c6-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="036c6-119">Lásd az alábbi példát.</span><span class="sxs-lookup"><span data-stu-id="036c6-119">See an example below.</span></span> 

<span data-ttu-id="036c6-120">__A kvóták esetében:__</span><span class="sxs-lookup"><span data-stu-id="036c6-120">__For quota tickets:__</span></span>

<span data-ttu-id="036c6-121">Ha a **VM-magok** , a **köteg** , az SQL- **adatbázis** és az **SQL-adattárház** kvótájának növelését szeretné kérni, további részleteket adhat meg a *QuotaTicketDetail* objektum csoportban.</span><span class="sxs-lookup"><span data-stu-id="036c6-121">To request for quota increase for **Compute VM Cores** , **Batch** , **SQL Database** and **SQL Data Warehouse** , provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="036c6-122">Az QuotaTicketDetail objektum 3 tulajdonságból áll, az alább leírt módon.</span><span class="sxs-lookup"><span data-stu-id="036c6-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="036c6-123">Részletes dokumentációért [kattintson ide.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="036c6-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="036c6-124">Ha részletesen szeretné tudni, hogy miként építhet fel hasznos tartalmakat a különféle kontingensek típusaira, [kattintson ide](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="036c6-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="036c6-125">Példák</span><span class="sxs-lookup"><span data-stu-id="036c6-125">EXAMPLES</span></span>

### <span data-ttu-id="036c6-126">Példa 1: számlázási vagy előfizetés-kezelési támogatási jegy létrehozása.</span><span class="sxs-lookup"><span data-stu-id="036c6-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="036c6-127">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a számlázási vagy az előfizetés-kezelési problémák helyes AZONOSÍTÓját, amelyre támogatást szeretne kérni</span><span class="sxs-lookup"><span data-stu-id="036c6-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-128">2. példa: terméktámogatási jegy létrehozása a virtuális gép Windows-erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="036c6-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="036c6-129">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a Windows-alapú virtuális gép megfelelő GUID-azonosítóit, amelyekre támogatást szeretne kérni</span><span class="sxs-lookup"><span data-stu-id="036c6-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-130">3. példa: kvóta-támogatási jegy létrehozása egy adott VM-családhoz tartozó virtuális gép magok kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="036c6-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="036c6-131">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével a kvóta kiszámításához a VM magok probléma besorolása című fejezet helyes GUID-elemeit olvashatja be.</span><span class="sxs-lookup"><span data-stu-id="036c6-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-132">Példa 4: kvóta-támogatási jegy létrehozása egy köteg-fiókban a kis prioritású magok kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="036c6-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="036c6-133">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta-használati problémák besorolásának megfelelő GUID-elemeit.</span><span class="sxs-lookup"><span data-stu-id="036c6-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-134">Példa 5: kvóta-támogatási jegy létrehozása egy adott VM-családhoz tartozó VM magok kvótájának növelése céljából egy köteg fiók esetén.</span><span class="sxs-lookup"><span data-stu-id="036c6-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="036c6-135">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta-használati problémák besorolásának megfelelő GUID-elemeit.</span><span class="sxs-lookup"><span data-stu-id="036c6-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-136">6. példa: kvóta-támogatási jegy létrehozása egy köteghez tartozó készlet kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="036c6-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="036c6-137">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta-használati problémák besorolásának megfelelő GUID-elemeit.</span><span class="sxs-lookup"><span data-stu-id="036c6-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-138">7. példa: kvóta-támogatási jegy létrehozása a kötegelt fiók aktív feladatainak és munkaütemezések kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="036c6-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="036c6-139">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta-használati problémák besorolásának megfelelő GUID-elemeit.</span><span class="sxs-lookup"><span data-stu-id="036c6-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-140">8. példa: kvóta-támogatási jegy létrehozása az előfizetéshez tartozó kötegelt fiókok számának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="036c6-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="036c6-141">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta-használati problémák besorolásának megfelelő GUID-elemeit.</span><span class="sxs-lookup"><span data-stu-id="036c6-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-142">9. példa: kvóta-támogatási jegy létrehozása az SQL-adatbázis DTU kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="036c6-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="036c6-143">Az Get-AzSupportService és a Get-AzSupportProblemClassification segítségével beolvashatja a kvóta SQL-adatbázis problémáinak besorolása című fejezet helyes GUID azonosítóit.</span><span class="sxs-lookup"><span data-stu-id="036c6-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-144">10. példa: kvóta-támogatási jegy létrehozása az SQL-adatbázis kiszolgálói kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="036c6-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="036c6-145">Az Get-AzSupportService és a Get-AzSupportProblemClassification segítségével beolvashatja a kvóta SQL-adatbázis problémáinak besorolása című fejezet helyes GUID azonosítóit.</span><span class="sxs-lookup"><span data-stu-id="036c6-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-146">11-es példa: kvóta-támogatási jegy létrehozása az SQL-adattárház DTU kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="036c6-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="036c6-147">Az Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta SQL Date Warehouse-probléma besorolásának megfelelő GUID-azonosítókat.</span><span class="sxs-lookup"><span data-stu-id="036c6-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-148">12 példa: kvóta-támogatási jegy létrehozása az SQL-adattárházban lévő kiszolgálók kvótájának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="036c6-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="036c6-149">A kvóta SQL-adatraktár problémáinak osztályozása az Get-AzSupportService és a Get-AzSupportProblemClassification használatával.</span><span class="sxs-lookup"><span data-stu-id="036c6-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-150">13. példa: kvóta-támogatási jegy létrehozása a kis prioritású magokra vonatkozó kvóta növeléséhez a gépi tanulási szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="036c6-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="036c6-151">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta-automaták tanulási szolgáltatási problémájának megfelelő GUID-azonosítókat.</span><span class="sxs-lookup"><span data-stu-id="036c6-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-152">14. példa: kvóta-támogatási jegy létrehozása a VM magok kvótájának növelése egy adott VM-családban a gépi tanulási szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="036c6-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="036c6-153">A Get-AzSupportService és a Get-AzSupportProblemClassification segítségével megkeresheti a kvóta-automaták tanulási szolgáltatási problémájának megfelelő GUID-azonosítókat.</span><span class="sxs-lookup"><span data-stu-id="036c6-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-154">15 példa: támogatási jegy létrehozása a CustomerContactDetail objektum helyett az egyes ügyfél-kapcsolatfelvételi paraméterek megadásával.</span><span class="sxs-lookup"><span data-stu-id="036c6-154">Example 15: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-155">16. példa: támogatási jegy létrehozása az Azure 24 x 7 válaszára vonatkozó kéréssel</span><span class="sxs-lookup"><span data-stu-id="036c6-155">Example 16: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="036c6-156">17. példa: a támogatási jegy létrehozása az ügyfél nevében a felhőalapú megoldás-szolgáltató (CSP) esetén.</span><span class="sxs-lookup"><span data-stu-id="036c6-156">Example 17: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="036c6-157">A CSP-nek először be kell jelentkeznie a bérlői webhelyre, majd be kell jelentkeznie az ügyfél bérlői webhelyére az alábbi példa szerint.</span><span class="sxs-lookup"><span data-stu-id="036c6-157">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="036c6-158">A támogatási jegy létrehozásakor a-CSPHomeTenantId paraméterrel meg kell adnia az otthoni bérlői azonosítót.</span><span class="sxs-lookup"><span data-stu-id="036c6-158">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="036c6-159">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="036c6-159">PARAMETERS</span></span>

### <span data-ttu-id="036c6-160">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="036c6-160">-AdditionalEmailAddress</span></span>
<span data-ttu-id="036c6-161">További e-mail-címek.</span><span class="sxs-lookup"><span data-stu-id="036c6-161">Additional email addresses.</span></span>
<span data-ttu-id="036c6-162">Az itt felsorolt e-mail-címeket a támogatási jegyre vonatkozó minden levelezésre másolhatja.</span><span class="sxs-lookup"><span data-stu-id="036c6-162">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="036c6-163">-AsJob</span><span class="sxs-lookup"><span data-stu-id="036c6-163">-AsJob</span></span>
<span data-ttu-id="036c6-164">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="036c6-164">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="036c6-165">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="036c6-165">-CSPHomeTenantId</span></span>
<span data-ttu-id="036c6-166">Ez a felhőalapú megoldás-szolgáltató felhasználó otthoni bérlői azonosítója, amellyel támogatási jegyet hozhat létre az ügyfél számára.</span><span class="sxs-lookup"><span data-stu-id="036c6-166">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

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

### <span data-ttu-id="036c6-167">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="036c6-167">-CustomerContactDetail</span></span>
<span data-ttu-id="036c6-168">Az SupportTicket-erőforráshoz társított ügyfél-elérhetőségi adatok.</span><span class="sxs-lookup"><span data-stu-id="036c6-168">Customer contact details associated with SupportTicket resource.</span></span>

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

### <span data-ttu-id="036c6-169">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="036c6-169">-CustomerCountry</span></span>
<span data-ttu-id="036c6-170">Ügyfél országa.</span><span class="sxs-lookup"><span data-stu-id="036c6-170">Customer country.</span></span>
<span data-ttu-id="036c6-171">A kódnak érvényes ISO Alpha-3 országkód (ISO 3166) kell lennie.</span><span class="sxs-lookup"><span data-stu-id="036c6-171">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="036c6-172">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="036c6-172">-CustomerFirstName</span></span>
<span data-ttu-id="036c6-173">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="036c6-173">Customer first name.</span></span>

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

### <span data-ttu-id="036c6-174">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="036c6-174">-CustomerLastName</span></span>
<span data-ttu-id="036c6-175">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="036c6-175">Customer last name.</span></span>

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

### <span data-ttu-id="036c6-176">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="036c6-176">-CustomerPhoneNumber</span></span>
<span data-ttu-id="036c6-177">Ügyfél telefonszáma.</span><span class="sxs-lookup"><span data-stu-id="036c6-177">Customer phone number.</span></span>
<span data-ttu-id="036c6-178">Erre akkor van szükség, ha az elsődleges névjegykártya-módszer telefon.</span><span class="sxs-lookup"><span data-stu-id="036c6-178">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="036c6-179">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="036c6-179">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="036c6-180">Az egyéni Peferred nyelve.</span><span class="sxs-lookup"><span data-stu-id="036c6-180">Peferred language of the custom.</span></span>
<span data-ttu-id="036c6-181">Ennek az itt felsorolt támogatott nyelvek egyikéhez érvényes célnyelv-kódnak kell lennie https://azure.microsoft.com/en-us/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="036c6-181">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

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

### <span data-ttu-id="036c6-182">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="036c6-182">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="036c6-183">Ügyfél által preferált időzóna</span><span class="sxs-lookup"><span data-stu-id="036c6-183">Customer preferred time zone.</span></span>
<span data-ttu-id="036c6-184">Ennek érvényes System.TimeZoneInfo.Id-értéknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="036c6-184">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="036c6-185">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="036c6-185">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="036c6-186">Ügyfél elsődleges e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="036c6-186">Customer primary email address.</span></span>

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

### <span data-ttu-id="036c6-187">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="036c6-187">-DefaultProfile</span></span>
<span data-ttu-id="036c6-188">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="036c6-188">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="036c6-189">-Leírás</span><span class="sxs-lookup"><span data-stu-id="036c6-189">-Description</span></span>
<span data-ttu-id="036c6-190">A kérdés vagy probléma részletes leírása.</span><span class="sxs-lookup"><span data-stu-id="036c6-190">Detailed description of the question or issue.</span></span>

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

### <span data-ttu-id="036c6-191">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="036c6-191">-Name</span></span>
<span data-ttu-id="036c6-192">A parancsmag által létrehozott támogatási jegy neve.</span><span class="sxs-lookup"><span data-stu-id="036c6-192">Name of support ticket that this cmdlet creates.</span></span>

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

### <span data-ttu-id="036c6-193">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="036c6-193">-PreferredContactMethod</span></span>
<span data-ttu-id="036c6-194">Preferált kontakt mód</span><span class="sxs-lookup"><span data-stu-id="036c6-194">Preferred contact method.</span></span>

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

### <span data-ttu-id="036c6-195">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="036c6-195">-ProblemClassificationId</span></span>
<span data-ttu-id="036c6-196">Minden Azure-szolgáltatáshoz tartozik egy saját, a problémára vonatkozó besorolási kategória, amely megfelel az észlelt probléma típusának.</span><span class="sxs-lookup"><span data-stu-id="036c6-196">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="036c6-197">Ez a paraméter a ProblemClassification-erőforrás ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="036c6-197">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

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

### <span data-ttu-id="036c6-198">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="036c6-198">-ProblemStartTime</span></span>
<span data-ttu-id="036c6-199">A probléma kezdetének dátuma és időpontja.</span><span class="sxs-lookup"><span data-stu-id="036c6-199">Date and time when the problem started.</span></span>

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

### <span data-ttu-id="036c6-200">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="036c6-200">-QuotaTicketDetail</span></span>
<span data-ttu-id="036c6-201">További részletek a kvóta-támogatási jegyekről.</span><span class="sxs-lookup"><span data-stu-id="036c6-201">Additional details for a Quota support ticket.</span></span>

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

### <span data-ttu-id="036c6-202">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="036c6-202">-Require24X7Response</span></span>
<span data-ttu-id="036c6-203">Jelzi, hogy ez a támogatási jegy az Azuretól kapott 24x7 választ igényli-e.</span><span class="sxs-lookup"><span data-stu-id="036c6-203">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

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

### <span data-ttu-id="036c6-204">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="036c6-204">-Severity</span></span>
<span data-ttu-id="036c6-205">A támogatási jegy súlyossága.</span><span class="sxs-lookup"><span data-stu-id="036c6-205">Severity of the support ticket.</span></span>
<span data-ttu-id="036c6-206">Ez jelzi az eset sürgősségét, ami viszont az Azure-szal kötött technikai támogatási csomag szolgáltatási szintről szóló szerződése szerint a válaszadás időpontját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="036c6-206">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

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

### <span data-ttu-id="036c6-207">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="036c6-207">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="036c6-208">Ez az Azure szolgáltatási erőforrás erőforrás-azonosítója (például: egy virtuális gép vagy egy HDInsight-erőforrás), amelyhez a támogatási jegyet létrehozta.</span><span class="sxs-lookup"><span data-stu-id="036c6-208">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

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

### <span data-ttu-id="036c6-209">-Cím</span><span class="sxs-lookup"><span data-stu-id="036c6-209">-Title</span></span>
<span data-ttu-id="036c6-210">A támogatási jegy címe.</span><span class="sxs-lookup"><span data-stu-id="036c6-210">Title of support ticket.</span></span>

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

### <span data-ttu-id="036c6-211">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="036c6-211">-Confirm</span></span>
<span data-ttu-id="036c6-212">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="036c6-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="036c6-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="036c6-213">-WhatIf</span></span>
<span data-ttu-id="036c6-214">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="036c6-214">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="036c6-215">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="036c6-215">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="036c6-216">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="036c6-216">CommonParameters</span></span>
<span data-ttu-id="036c6-217">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="036c6-217">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="036c6-218">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="036c6-218">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="036c6-219">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="036c6-219">INPUTS</span></span>

### <span data-ttu-id="036c6-220">Nincs</span><span class="sxs-lookup"><span data-stu-id="036c6-220">None</span></span>

## <span data-ttu-id="036c6-221">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="036c6-221">OUTPUTS</span></span>

### <span data-ttu-id="036c6-222">Microsoft. Azure. commands. support. models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="036c6-222">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="036c6-223">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="036c6-223">NOTES</span></span>

## <span data-ttu-id="036c6-224">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="036c6-224">RELATED LINKS</span></span>
