---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: c5bbe6413a17707e7c25a616c3c67d6b7d5da5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501248"
---
# <span data-ttu-id="c72bc-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c72bc-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="c72bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c72bc-102">SYNOPSIS</span></span>
<span data-ttu-id="c72bc-103">API-kezelési csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c72bc-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c72bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c72bc-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c72bc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c72bc-105">DESCRIPTION</span></span>
<span data-ttu-id="c72bc-106">A **New-AzureRmApiManagementGroup** PARANCSMAG egy API-kezelési csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c72bc-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="c72bc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c72bc-107">EXAMPLES</span></span>

### <span data-ttu-id="c72bc-108">Példa 1: felügyeleti csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="c72bc-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="c72bc-109">A parancs létrehoz egy felügyeleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="c72bc-109">This command creates a management group.</span></span>

## <span data-ttu-id="c72bc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c72bc-110">PARAMETERS</span></span>

### <span data-ttu-id="c72bc-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c72bc-111">-Context</span></span>
<span data-ttu-id="c72bc-112">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c72bc-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c72bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c72bc-113">-DefaultProfile</span></span>
<span data-ttu-id="c72bc-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c72bc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c72bc-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c72bc-115">-Description</span></span>
<span data-ttu-id="c72bc-116">A kezelési csoport leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c72bc-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="c72bc-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="c72bc-117">-ExternalId</span></span>
<span data-ttu-id="c72bc-118">A külső csoportok esetében ez a tulajdonság a külső identitás-szolgáltatótól származó csoport azonosítóját tartalmazza, például az Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; máskülönben az érték null.</span><span class="sxs-lookup"><span data-stu-id="c72bc-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="c72bc-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="c72bc-119">-GroupId</span></span>
<span data-ttu-id="c72bc-120">Az új felügyeleti csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c72bc-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="c72bc-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c72bc-121">-Name</span></span>
<span data-ttu-id="c72bc-122">A felügyeleti csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c72bc-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="c72bc-123">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="c72bc-123">-Type</span></span>
<span data-ttu-id="c72bc-124">Csoport típusa.</span><span class="sxs-lookup"><span data-stu-id="c72bc-124">Group Type.</span></span> <span data-ttu-id="c72bc-125">Az egyéni csoport a felhasználó által definiált csoport.</span><span class="sxs-lookup"><span data-stu-id="c72bc-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="c72bc-126">A Rendszercsoport a rendszergazda, a fejlesztők és a vendégek elemre is kiterjed.</span><span class="sxs-lookup"><span data-stu-id="c72bc-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="c72bc-127">Nem hozhat létre és nem frissíthet rendszercsoportot.</span><span class="sxs-lookup"><span data-stu-id="c72bc-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="c72bc-128">Külső csoport: az Azure Active Directory szolgáltatója, például a külső identitás szolgáltatója.</span><span class="sxs-lookup"><span data-stu-id="c72bc-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="c72bc-129">Ez a paraméter nem kötelező, és alapértelmezés szerint egyéni csoportnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c72bc-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

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

### <span data-ttu-id="c72bc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c72bc-130">CommonParameters</span></span>
<span data-ttu-id="c72bc-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c72bc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c72bc-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c72bc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c72bc-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c72bc-133">INPUTS</span></span>

### <span data-ttu-id="c72bc-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c72bc-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c72bc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c72bc-135">System.String</span></span>

### <span data-ttu-id="c72bc-136">System. null ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementGroupType, Microsoft. Azure. commands. ApiManagement. ServiceManagement, Version = 6.1.0.0</span><span class="sxs-lookup"><span data-stu-id="c72bc-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c72bc-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c72bc-137">OUTPUTS</span></span>

### <span data-ttu-id="c72bc-138">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c72bc-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="c72bc-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c72bc-139">NOTES</span></span>

## <span data-ttu-id="c72bc-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c72bc-140">RELATED LINKS</span></span>

[<span data-ttu-id="c72bc-141">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c72bc-141">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="c72bc-142">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c72bc-142">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="c72bc-143">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c72bc-143">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


