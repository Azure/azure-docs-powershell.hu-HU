---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: 22feec8308b682aa2290de6bd8b7361bb07cd560
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671672"
---
# <span data-ttu-id="41028-101">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="41028-101">New-AzApiManagementGroup</span></span>

## <span data-ttu-id="41028-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41028-102">SYNOPSIS</span></span>
<span data-ttu-id="41028-103">API-kezelési csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="41028-103">Creates an API management group.</span></span>

## <span data-ttu-id="41028-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41028-104">SYNTAX</span></span>

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41028-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="41028-105">DESCRIPTION</span></span>
<span data-ttu-id="41028-106">A **New-AzApiManagementGroup** PARANCSMAG egy API-kezelési csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="41028-106">The **New-AzApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="41028-107">Példák</span><span class="sxs-lookup"><span data-stu-id="41028-107">EXAMPLES</span></span>

### <span data-ttu-id="41028-108">Példa 1: felügyeleti csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="41028-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="41028-109">A parancs létrehoz egy felügyeleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="41028-109">This command creates a management group.</span></span>

## <span data-ttu-id="41028-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41028-110">PARAMETERS</span></span>

### <span data-ttu-id="41028-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="41028-111">-Context</span></span>
<span data-ttu-id="41028-112">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41028-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="41028-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41028-113">-DefaultProfile</span></span>
<span data-ttu-id="41028-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41028-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41028-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="41028-115">-Description</span></span>
<span data-ttu-id="41028-116">A kezelési csoport leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="41028-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="41028-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="41028-117">-ExternalId</span></span>
<span data-ttu-id="41028-118">A külső csoportok esetében ez a tulajdonság a külső identitás-szolgáltatótól származó csoport azonosítóját tartalmazza, például az Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; máskülönben az érték null.</span><span class="sxs-lookup"><span data-stu-id="41028-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="41028-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="41028-119">-GroupId</span></span>
<span data-ttu-id="41028-120">Az új felügyeleti csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="41028-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="41028-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41028-121">-Name</span></span>
<span data-ttu-id="41028-122">A felügyeleti csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41028-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="41028-123">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="41028-123">-Type</span></span>
<span data-ttu-id="41028-124">Csoport típusa.</span><span class="sxs-lookup"><span data-stu-id="41028-124">Group Type.</span></span> <span data-ttu-id="41028-125">Az egyéni csoport a felhasználó által definiált csoport.</span><span class="sxs-lookup"><span data-stu-id="41028-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="41028-126">A Rendszercsoport a rendszergazda, a fejlesztők és a vendégek elemre is kiterjed.</span><span class="sxs-lookup"><span data-stu-id="41028-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="41028-127">Nem hozhat létre és nem frissíthet rendszercsoportot.</span><span class="sxs-lookup"><span data-stu-id="41028-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="41028-128">Külső csoport: az Azure Active Directory szolgáltatója, például a külső identitás szolgáltatója.</span><span class="sxs-lookup"><span data-stu-id="41028-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="41028-129">Ez a paraméter nem kötelező, és alapértelmezés szerint egyéni csoportnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="41028-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System, External

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41028-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41028-130">CommonParameters</span></span>
<span data-ttu-id="41028-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41028-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41028-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41028-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41028-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41028-133">INPUTS</span></span>

### <span data-ttu-id="41028-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="41028-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="41028-135">System. String</span><span class="sxs-lookup"><span data-stu-id="41028-135">System.String</span></span>

### <span data-ttu-id="41028-136">System. nulla ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementGroupType, Microsoft. Azure. PowerShell. parancsmagok. ApiManagement. ServiceManagement, Version = 1.0.0.0, = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="41028-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="41028-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41028-137">OUTPUTS</span></span>

### <span data-ttu-id="41028-138">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="41028-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="41028-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41028-139">NOTES</span></span>

## <span data-ttu-id="41028-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41028-140">RELATED LINKS</span></span>

[<span data-ttu-id="41028-141">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="41028-141">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="41028-142">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="41028-142">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="41028-143">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="41028-143">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


