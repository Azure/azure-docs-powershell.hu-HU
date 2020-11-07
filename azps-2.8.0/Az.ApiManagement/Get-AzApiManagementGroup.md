---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: 9a8acd17f953e90cd5b4311854830da03dc4df0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668113"
---
# <span data-ttu-id="5022f-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5022f-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="5022f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5022f-102">SYNOPSIS</span></span>
<span data-ttu-id="5022f-103">Az API-adatkezelési csoportok teljes vagy konkrét beolvasása</span><span class="sxs-lookup"><span data-stu-id="5022f-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="5022f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5022f-104">SYNTAX</span></span>

### <span data-ttu-id="5022f-105">GetAllGroups (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5022f-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5022f-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="5022f-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5022f-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="5022f-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5022f-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="5022f-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5022f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5022f-109">DESCRIPTION</span></span>
<span data-ttu-id="5022f-110">A **Get-AzApiManagementGroup** parancsmag a teljes vagy bizonyos API-kezelési csoportokat kapja.</span><span class="sxs-lookup"><span data-stu-id="5022f-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="5022f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5022f-111">EXAMPLES</span></span>

### <span data-ttu-id="5022f-112">Példa 1: az összes csoport beolvasása</span><span class="sxs-lookup"><span data-stu-id="5022f-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="5022f-113">Ez a parancs az összes csoportot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="5022f-113">This command gets all groups.</span></span>

### <span data-ttu-id="5022f-114">2. példa: csoport beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="5022f-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="5022f-115">Ez a parancs a 0123456789 nevű csoport AZONOSÍTÓját kapja.</span><span class="sxs-lookup"><span data-stu-id="5022f-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="5022f-116">3. példa: csoport beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="5022f-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="5022f-117">Ez a parancs a Group0002 nevű csoportot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5022f-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="5022f-118">4. példa: az összes felhasználó csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="5022f-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="5022f-119">Ez a parancs a 0123456789 nevű felhasználói AZONOSÍTÓval minden felhasználó csoportba bekerül.</span><span class="sxs-lookup"><span data-stu-id="5022f-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="5022f-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5022f-120">PARAMETERS</span></span>

### <span data-ttu-id="5022f-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5022f-121">-Context</span></span>
<span data-ttu-id="5022f-122">A PsApiManagementContext példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5022f-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="5022f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5022f-123">-DefaultProfile</span></span>
<span data-ttu-id="5022f-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5022f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5022f-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="5022f-125">-GroupId</span></span>
<span data-ttu-id="5022f-126">A csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5022f-126">Specifies the group ID.</span></span>
<span data-ttu-id="5022f-127">Ha meg van adva, a parancsmag megpróbálja megtalálni a csoportot az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="5022f-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGroupId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5022f-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5022f-128">-Name</span></span>
<span data-ttu-id="5022f-129">A felügyeleti csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5022f-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="5022f-130">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="5022f-130">-ProductId</span></span>
<span data-ttu-id="5022f-131">A meglévő szorzat azonosítója</span><span class="sxs-lookup"><span data-stu-id="5022f-131">Identifier of existing product.</span></span>
<span data-ttu-id="5022f-132">Ha meg van adva, akkor a rendszer minden olyan csoportot ad vissza, amelyre a terméket hozzárendeli.</span><span class="sxs-lookup"><span data-stu-id="5022f-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="5022f-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5022f-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5022f-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="5022f-134">-UserId</span></span>
<span data-ttu-id="5022f-135">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5022f-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="5022f-136">Ha meg van adva, a parancsmag minden olyan csoportot ad vissza, amelyre a terméket hozzárendeli.</span><span class="sxs-lookup"><span data-stu-id="5022f-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5022f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5022f-137">CommonParameters</span></span>
<span data-ttu-id="5022f-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5022f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5022f-139">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5022f-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5022f-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5022f-140">INPUTS</span></span>

### <span data-ttu-id="5022f-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5022f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5022f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5022f-142">System.String</span></span>

## <span data-ttu-id="5022f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5022f-143">OUTPUTS</span></span>

### <span data-ttu-id="5022f-144">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5022f-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="5022f-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5022f-145">NOTES</span></span>

## <span data-ttu-id="5022f-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5022f-146">RELATED LINKS</span></span>

[<span data-ttu-id="5022f-147">Új – AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5022f-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="5022f-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5022f-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="5022f-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5022f-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


