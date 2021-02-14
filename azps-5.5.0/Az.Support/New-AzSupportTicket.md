---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150051"
---
# <span data-ttu-id="f326e-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="f326e-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="f326e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f326e-102">SYNOPSIS</span></span>
<span data-ttu-id="f326e-103">Létrehoz egy támogatási jegyet.</span><span class="sxs-lookup"><span data-stu-id="f326e-103">Creates a support ticket.</span></span>

## <span data-ttu-id="f326e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f326e-104">SYNTAX</span></span>

### <span data-ttu-id="f326e-105">CreateSupportTicketWithContactDetailParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f326e-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f326e-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f326e-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f326e-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f326e-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f326e-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f326e-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f326e-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="f326e-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f326e-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="f326e-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f326e-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f326e-111">DESCRIPTION</span></span>
<span data-ttu-id="f326e-112">Ezzel a parancsmagtal létrehozhat egy támogatási jegyet számlázási, előfizetés-kezelési, kvóta- vagy technikai problémákhoz.</span><span class="sxs-lookup"><span data-stu-id="f326e-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="f326e-113">A Get-AzSupportService és Get-AzSupportProblemClassification segítségével azonosítsa az Azure-szolgáltatást, és a megfelelő problémabesorolásokat, amelyekhez támogatást szeretne kérni.</span><span class="sxs-lookup"><span data-stu-id="f326e-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="f326e-114">A következő paramétereket kell megadnia:</span><span class="sxs-lookup"><span data-stu-id="f326e-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="f326e-115">A CustomerContactDetail New-AzSupportContactProfileObject létrehozhatja a CustomerContactDetail objektumot egy segítő parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="f326e-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="f326e-116">A felhőszolgáltatók támogatási jegyet hozhatnak létre ügyfeleik előfizetéséhez, ha bejelentkeznek az ügyfél bérlőjébe, és a *CSPHomeTenantId* paramétert használva meg kell adniuk az otthoni bérlőazonosítójukat.</span><span class="sxs-lookup"><span data-stu-id="f326e-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="f326e-117">__Műszaki jegyek:__</span><span class="sxs-lookup"><span data-stu-id="f326e-117">__For technical tickets:__</span></span>

<span data-ttu-id="f326e-118">Az erőforrás nevének megadásához adja meg az ARM erőforrás-azonosítóját a *TechnicalTicketResourceId* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="f326e-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="f326e-119">Alább láthat egy példát.</span><span class="sxs-lookup"><span data-stu-id="f326e-119">See an example below.</span></span> 

<span data-ttu-id="f326e-120">__Kvóta-jegyek esetében:__</span><span class="sxs-lookup"><span data-stu-id="f326e-120">__For quota tickets:__</span></span>

<span data-ttu-id="f326e-121">A VM-alapmagok, a **Batch,** az **SQL-adatbázis** és az **SQL-adattárhely** kvótaemelésének kéréséhez adjon meg további részleteket a *QuotaTicketDetail* objektumban. </span><span class="sxs-lookup"><span data-stu-id="f326e-121">To request for quota increase for **Compute VM Cores**, **Batch**, **SQL Database** and **SQL Data Warehouse**, provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="f326e-122">A QuotaTicketDetail objektum 3 tulajdonságból áll, az alábbiakban ismertetett módon.</span><span class="sxs-lookup"><span data-stu-id="f326e-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="f326e-123">A részletes dokumentációért kattintson [ide.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="f326e-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

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


<span data-ttu-id="f326e-124">A különböző kvótatípusokhoz szükséges hasznos terhelések felépítéséről részletes dokumentációt [itt talál.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="f326e-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="f326e-125">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f326e-125">EXAMPLES</span></span>

### <span data-ttu-id="f326e-126">1. példa: Számlázási vagy Előfizetéskezelési támogatási jegy létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f326e-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="f326e-127">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a számlázással vagy előfizetés-kezeléssel kapcsolatos problémabesorolás helyes GUID azonosítóit, amelyekhez támogatást szeretne kérni</span><span class="sxs-lookup"><span data-stu-id="f326e-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-128">2. példa: Hozzon létre egy technikai támogatási jegyet a Virtuális gép Windows-erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="f326e-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="f326e-129">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a windowsos virtuális gép problémabesorolásának helyes GUID-ját, amelyhez támogatást szeretne kérni</span><span class="sxs-lookup"><span data-stu-id="f326e-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-130">3. példa: Hozzon létre egy kvóta-támogatási jegyet a virtuális gépi alapmagok kvótája egy adott VM-családhoz való növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f326e-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="f326e-131">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a megfelelő GUID-azonosítókat a kvóta-számítási VIRTUÁLIS GÉPmagok problémabesorolásához.</span><span class="sxs-lookup"><span data-stu-id="f326e-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-132">4. példa: Hozzon létre egy kvóta-támogatási jegyet az alacsony prioritású magok kvótája növeléséhez egy Batch-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f326e-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="f326e-133">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a helyes GUID azonosítókat a Kvótakötet problémabesorolásához.</span><span class="sxs-lookup"><span data-stu-id="f326e-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-134">5. példa: Kvóta-támogatási jegy létrehozása a VM-alapkvóta növeléséhez egy adott VM-családhoz egy Batch-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f326e-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="f326e-135">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a helyes GUID azonosítókat a Kvótakötet problémabesorolásához.</span><span class="sxs-lookup"><span data-stu-id="f326e-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-136">6. példa: Kvóta-támogatási jegy létrehozása a Kötegfiók készletkvótája növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f326e-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="f326e-137">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a helyes GUID azonosítókat a Kvótakötet problémabesorolásához.</span><span class="sxs-lookup"><span data-stu-id="f326e-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-138">7. példa: Kvóta-támogatási jegy létrehozása egy Batch-fiók aktív feladatokra és beosztásokra vonatkozó kvótája növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f326e-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="f326e-139">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a helyes GUID azonosítókat a Kvótakötet problémabesorolásához.</span><span class="sxs-lookup"><span data-stu-id="f326e-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-140">8. példa: Kvóta-támogatási jegy létrehozása egy előfizetés Kötegfiókok számának növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f326e-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="f326e-141">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a helyes GUID azonosítókat a Kvótakötet problémabesorolásához.</span><span class="sxs-lookup"><span data-stu-id="f326e-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-142">9. példa: Kvóta-támogatási jegy létrehozása az SQL-adatbázis DTUs-kvótája növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f326e-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="f326e-143">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a megfelelő GUID azonosítókat a Kvóta SQL-adatbázis problémabesorolásához.</span><span class="sxs-lookup"><span data-stu-id="f326e-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-144">10. példa: Kvóta-támogatási jegy létrehozása az SQL-adatbázis kiszolgálói kvótája növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f326e-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="f326e-145">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a megfelelő GUID azonosítókat a Kvóta SQL-adatbázis problémabesorolásához.</span><span class="sxs-lookup"><span data-stu-id="f326e-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-146">11. példa: Kvóta-támogatási jegy létrehozása az SQL-adattárhely DTUs-kvótája növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f326e-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="f326e-147">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a megfelelő GUID azonosítókat az SQL-dátumtárhely problémabesorolásához.</span><span class="sxs-lookup"><span data-stu-id="f326e-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-148">12. példa: Kvóta-támogatási jegy létrehozása az SQL-adattárhely kiszolgálói kvótája növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f326e-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="f326e-149">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a megfelelő GUID azonosítókat a Kvóta SQL-adattárház problémabesorolásához.</span><span class="sxs-lookup"><span data-stu-id="f326e-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-150">13. példa: Kvóta-támogatási jegy létrehozása az alacsony prioritású magok kvótája növeléséhez a Gépi tanulás szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="f326e-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="f326e-151">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a helyes GUID azonosítókat a Quota Machine Learning szolgáltatás problémabesorolásához.</span><span class="sxs-lookup"><span data-stu-id="f326e-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-152">14. példa: Kvóta-támogatási jegy létrehozása a VM-alapkvóta növeléséhez egy adott GÉPI gépi tanulás szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="f326e-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="f326e-153">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a helyes GUID azonosítókat a Quota Machine Learning szolgáltatás problémabesorolásához.</span><span class="sxs-lookup"><span data-stu-id="f326e-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-154">15. példa: Kvóta-támogatási jegy létrehozása az Azure SQL Felügyelt példány kvótája növeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f326e-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="f326e-155">A Get-AzSupportService és Get-AzSupportProblemClassification lekéri a megfelelő GUID azonosítókat az SQL Felügyelt példány szolgáltatás problémabesorolásához.</span><span class="sxs-lookup"><span data-stu-id="f326e-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-156">16. példa: Támogatási jegy létrehozása a CustomerContactDetail objektum helyett egyéni ügyfélkapcsolati paraméterek megadásával.</span><span class="sxs-lookup"><span data-stu-id="f326e-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-157">17. példa: Hozzon létre egy támogatási jegyet az Azure-tól 24:7-es válaszkéréssel.</span><span class="sxs-lookup"><span data-stu-id="f326e-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f326e-158">18. példa: Hozzon létre egy támogatási jegyet az ügyfél nevében, ha Ön felhőszolgáltató.</span><span class="sxs-lookup"><span data-stu-id="f326e-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="f326e-159">A szolgáltatónak először be kell jelentkeznie a bérlői fiókba, majd be kell jelentkeznie az ügyfél bérlőjébe, az alábbi példában látható módon.</span><span class="sxs-lookup"><span data-stu-id="f326e-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="f326e-160">Ezután a -CSPHomeTenantId paramétert kell használniuk az otthoni bérlőazonosítójuk megadásához a támogatási jegy létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="f326e-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="f326e-161">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f326e-161">PARAMETERS</span></span>

### <span data-ttu-id="f326e-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f326e-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="f326e-163">További e-mail-címek.</span><span class="sxs-lookup"><span data-stu-id="f326e-163">Additional email addresses.</span></span>
<span data-ttu-id="f326e-164">Az itt felsorolt e-mail-címeket a rendszer a támogatási jegyről szóló minden levélre átmásolja.</span><span class="sxs-lookup"><span data-stu-id="f326e-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="f326e-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f326e-165">-AsJob</span></span>
<span data-ttu-id="f326e-166">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="f326e-166">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f326e-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="f326e-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="f326e-168">Ez annak a felhőszolgáltató felhasználónak az otthoni bérlői azonosítója, aki támogatási jegyet próbál létrehozni az ügyfél számára.</span><span class="sxs-lookup"><span data-stu-id="f326e-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

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

### <span data-ttu-id="f326e-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="f326e-169">-CustomerContactDetail</span></span>
<span data-ttu-id="f326e-170">A SupportTicket erőforráshoz társított ügyfélkapcsolati adatok.</span><span class="sxs-lookup"><span data-stu-id="f326e-170">Customer contact details associated with SupportTicket resource.</span></span>

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

### <span data-ttu-id="f326e-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="f326e-171">-CustomerCountry</span></span>
<span data-ttu-id="f326e-172">Ügyfél országa.</span><span class="sxs-lookup"><span data-stu-id="f326e-172">Customer country.</span></span>
<span data-ttu-id="f326e-173">Érvényes ISO Alfa-3 országkódnak (ISO 3166) kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f326e-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="f326e-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="f326e-174">-CustomerFirstName</span></span>
<span data-ttu-id="f326e-175">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="f326e-175">Customer first name.</span></span>

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

### <span data-ttu-id="f326e-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="f326e-176">-CustomerLastName</span></span>
<span data-ttu-id="f326e-177">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="f326e-177">Customer last name.</span></span>

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

### <span data-ttu-id="f326e-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="f326e-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="f326e-179">Ügyfél telefonszáma.</span><span class="sxs-lookup"><span data-stu-id="f326e-179">Customer phone number.</span></span>
<span data-ttu-id="f326e-180">Erre akkor van szükség, ha az előnyben részesített kapcsolatfelvételi mód a telefon.</span><span class="sxs-lookup"><span data-stu-id="f326e-180">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="f326e-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="f326e-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="f326e-182">Az egyéni nyelv kikövetkeztetve.</span><span class="sxs-lookup"><span data-stu-id="f326e-182">Peferred language of the custom.</span></span>
<span data-ttu-id="f326e-183">A kódnak érvényesnek kell lennie az itt felsorolt nyelvek https://azure.microsoft.com/en-us/support/faq/ egyikének.</span><span class="sxs-lookup"><span data-stu-id="f326e-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

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

### <span data-ttu-id="f326e-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="f326e-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="f326e-185">Ügyfél által előnyben részesített időzóna.</span><span class="sxs-lookup"><span data-stu-id="f326e-185">Customer preferred time zone.</span></span>
<span data-ttu-id="f326e-186">Ennek érvényes System.TimeZoneInfo.Id kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f326e-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="f326e-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f326e-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="f326e-188">Ügyfél elsődleges e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="f326e-188">Customer primary email address.</span></span>

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

### <span data-ttu-id="f326e-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f326e-189">-DefaultProfile</span></span>
<span data-ttu-id="f326e-190">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f326e-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f326e-191">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f326e-191">-Description</span></span>
<span data-ttu-id="f326e-192">A kérdés vagy probléma részletes leírása.</span><span class="sxs-lookup"><span data-stu-id="f326e-192">Detailed description of the question or issue.</span></span>

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

### <span data-ttu-id="f326e-193">-Name</span><span class="sxs-lookup"><span data-stu-id="f326e-193">-Name</span></span>
<span data-ttu-id="f326e-194">A parancsmag által létrehozott támogatási jegy neve.</span><span class="sxs-lookup"><span data-stu-id="f326e-194">Name of support ticket that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f326e-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="f326e-195">-PreferredContactMethod</span></span>
<span data-ttu-id="f326e-196">Előnyben részesített kapcsolatfelvételi mód.</span><span class="sxs-lookup"><span data-stu-id="f326e-196">Preferred contact method.</span></span>

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

### <span data-ttu-id="f326e-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="f326e-197">-ProblemClassificationId</span></span>
<span data-ttu-id="f326e-198">Mindegyik Azure-szolgáltatásnak saját problémakategóriája van, a probléma besorolása, amely megfelel a tapasztalt probléma típusának.</span><span class="sxs-lookup"><span data-stu-id="f326e-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="f326e-199">Ez a paraméter a ARM erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="f326e-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

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

### <span data-ttu-id="f326e-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="f326e-200">-ProblemStartTime</span></span>
<span data-ttu-id="f326e-201">A probléma elkezdődött dátuma és időpontja.</span><span class="sxs-lookup"><span data-stu-id="f326e-201">Date and time when the problem started.</span></span>

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

### <span data-ttu-id="f326e-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="f326e-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="f326e-203">További részletek a Kvóta támogatási jegyről.</span><span class="sxs-lookup"><span data-stu-id="f326e-203">Additional details for a Quota support ticket.</span></span>

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

### <span data-ttu-id="f326e-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="f326e-204">-Require24X7Response</span></span>
<span data-ttu-id="f326e-205">Azt jelzi, hogy a támogatási jegyhez az Azure a nap 24 órán belül választ igényel-e.</span><span class="sxs-lookup"><span data-stu-id="f326e-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

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

### <span data-ttu-id="f326e-206">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="f326e-206">-Severity</span></span>
<span data-ttu-id="f326e-207">A támogatási jegy súlyossága.</span><span class="sxs-lookup"><span data-stu-id="f326e-207">Severity of the support ticket.</span></span>
<span data-ttu-id="f326e-208">Ez az eset sürgősségére utal, amely az Azure-ral kötött technikai támogatási terv szolgáltatásiszint-szerződésének megfelelően határozza meg a válaszidőt.</span><span class="sxs-lookup"><span data-stu-id="f326e-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

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

### <span data-ttu-id="f326e-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="f326e-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="f326e-210">Ez annak az Azure szolgáltatáserőforrásnak az erőforrás-azonosítója (például: Virtuális gép típusú erőforrás vagy HDInsight-erőforrás), amelyhez a támogatási jegyet létrehozták.</span><span class="sxs-lookup"><span data-stu-id="f326e-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

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

### <span data-ttu-id="f326e-211">-Title</span><span class="sxs-lookup"><span data-stu-id="f326e-211">-Title</span></span>
<span data-ttu-id="f326e-212">A támogatási jegy címe.</span><span class="sxs-lookup"><span data-stu-id="f326e-212">Title of support ticket.</span></span>

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

### <span data-ttu-id="f326e-213">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f326e-213">-Confirm</span></span>
<span data-ttu-id="f326e-214">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f326e-214">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f326e-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f326e-215">-WhatIf</span></span>
<span data-ttu-id="f326e-216">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f326e-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f326e-217">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f326e-217">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f326e-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f326e-218">CommonParameters</span></span>
<span data-ttu-id="f326e-219">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f326e-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f326e-220">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f326e-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f326e-221">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f326e-221">INPUTS</span></span>

### <span data-ttu-id="f326e-222">Nincs</span><span class="sxs-lookup"><span data-stu-id="f326e-222">None</span></span>

## <span data-ttu-id="f326e-223">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f326e-223">OUTPUTS</span></span>

### <span data-ttu-id="f326e-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="f326e-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="f326e-225">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f326e-225">NOTES</span></span>

## <span data-ttu-id="f326e-226">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f326e-226">RELATED LINKS</span></span>
