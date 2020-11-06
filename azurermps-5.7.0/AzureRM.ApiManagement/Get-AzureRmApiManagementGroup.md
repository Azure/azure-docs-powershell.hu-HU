---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: b77452bff93a9b66f8ffe54fdff623d391749622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500632"
---
# <span data-ttu-id="4e3d7-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4e3d7-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="4e3d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e3d7-102">SYNOPSIS</span></span>
<span data-ttu-id="4e3d7-103">Az API-adatkezelési csoportok teljes vagy konkrét beolvasása</span><span class="sxs-lookup"><span data-stu-id="4e3d7-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e3d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e3d7-104">SYNTAX</span></span>

### <span data-ttu-id="4e3d7-105">GetAllGroups (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e3d7-105">GetAllGroups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e3d7-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="4e3d7-106">GetByGroupId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e3d7-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="4e3d7-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e3d7-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="4e3d7-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e3d7-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e3d7-109">DESCRIPTION</span></span>
<span data-ttu-id="4e3d7-110">A **Get-AzureRmApiManagementGroup** parancsmag a teljes vagy bizonyos API-kezelési csoportokat kapja.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="4e3d7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4e3d7-111">EXAMPLES</span></span>

### <span data-ttu-id="4e3d7-112">Példa 1: az összes csoport beolvasása</span><span class="sxs-lookup"><span data-stu-id="4e3d7-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext
```

<span data-ttu-id="4e3d7-113">Ez a parancs az összes csoportot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-113">This command gets all groups.</span></span>

### <span data-ttu-id="4e3d7-114">2. példa: csoport beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="4e3d7-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="4e3d7-115">Ez a parancs a 0123456789 nevű csoport AZONOSÍTÓját kapja.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="4e3d7-116">3. példa: csoport beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="4e3d7-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="4e3d7-117">Ez a parancs a Group0002 nevű csoportot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="4e3d7-118">4. példa: az összes felhasználó csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="4e3d7-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="4e3d7-119">Ez a parancs a 0123456789 nevű felhasználói AZONOSÍTÓval minden felhasználó csoportba bekerül.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="4e3d7-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e3d7-120">PARAMETERS</span></span>

### <span data-ttu-id="4e3d7-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4e3d7-121">-Context</span></span>
<span data-ttu-id="4e3d7-122">A PsApiManagementContext példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e3d7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e3d7-123">-DefaultProfile</span></span>
<span data-ttu-id="4e3d7-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e3d7-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="4e3d7-125">-GroupId</span></span>
<span data-ttu-id="4e3d7-126">A csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-126">Specifies the group ID.</span></span>
<span data-ttu-id="4e3d7-127">Ha meg van adva, a parancsmag megpróbálja megtalálni a csoportot az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByGroupId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e3d7-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e3d7-128">-Name</span></span>
<span data-ttu-id="4e3d7-129">A felügyeleti csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-129">Specifies the name of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e3d7-130">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="4e3d7-130">-ProductId</span></span>
<span data-ttu-id="4e3d7-131">A meglévő szorzat azonosítója</span><span class="sxs-lookup"><span data-stu-id="4e3d7-131">Identifier of existing product.</span></span>
<span data-ttu-id="4e3d7-132">Ha meg van adva, akkor a rendszer minden olyan csoportot ad vissza, amelyre a terméket hozzárendeli.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="4e3d7-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e3d7-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="4e3d7-134">-UserId</span></span>
<span data-ttu-id="4e3d7-135">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="4e3d7-136">Ha meg van adva, a parancsmag minden olyan csoportot ad vissza, amelyre a terméket hozzárendeli.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e3d7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e3d7-137">CommonParameters</span></span>
<span data-ttu-id="4e3d7-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e3d7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e3d7-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e3d7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e3d7-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e3d7-140">INPUTS</span></span>

### <span data-ttu-id="4e3d7-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="4e3d7-141">None</span></span>
<span data-ttu-id="4e3d7-142">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e3d7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e3d7-143">OUTPUTS</span></span>

### <span data-ttu-id="4e3d7-144">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4e3d7-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>
<span data-ttu-id="4e3d7-145">Az API-kezelési szolgáltatásban konfigurált csoport adatai.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-145">The details of the Group configured in API Management service.</span></span>

### <span data-ttu-id="4e3d7-146">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGroup></span><span class="sxs-lookup"><span data-stu-id="4e3d7-146">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>
<span data-ttu-id="4e3d7-147">Az API-kezelési szolgáltatásban konfigurált csoportok listája.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-147">The list of Groups configured in API Management service.</span></span>

## <span data-ttu-id="4e3d7-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e3d7-148">NOTES</span></span>

## <span data-ttu-id="4e3d7-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e3d7-149">RELATED LINKS</span></span>

[<span data-ttu-id="4e3d7-150">Új – AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4e3d7-150">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="4e3d7-151">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4e3d7-151">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="4e3d7-152">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4e3d7-152">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


