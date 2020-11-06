---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0c28742eb3c774adb8c7b6a8d920e91377bea35f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499280"
---
# <span data-ttu-id="baa85-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="baa85-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="baa85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="baa85-102">SYNOPSIS</span></span>
<span data-ttu-id="baa85-103">Az API-adatkezelési csoportok teljes vagy konkrét beolvasása</span><span class="sxs-lookup"><span data-stu-id="baa85-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baa85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="baa85-104">SYNTAX</span></span>

### <span data-ttu-id="baa85-105">Az összes csoport beolvasása (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="baa85-105">Get all groups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baa85-106">A beolvasás csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="baa85-106">Get by group ID</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baa85-107">Csoportok keresése felhasználó szerint</span><span class="sxs-lookup"><span data-stu-id="baa85-107">Find groups by user</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baa85-108">Csoportok keresése termékenként</span><span class="sxs-lookup"><span data-stu-id="baa85-108">Find groups by product</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baa85-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="baa85-109">DESCRIPTION</span></span>
<span data-ttu-id="baa85-110">A **Get-AzureRmApiManagementGroup** parancsmag a teljes vagy bizonyos API-kezelési csoportokat kapja.</span><span class="sxs-lookup"><span data-stu-id="baa85-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="baa85-111">Példák</span><span class="sxs-lookup"><span data-stu-id="baa85-111">EXAMPLES</span></span>

### <span data-ttu-id="baa85-112">Példa 1: az összes csoport beolvasása</span><span class="sxs-lookup"><span data-stu-id="baa85-112">Example 1: Get all groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext
```

<span data-ttu-id="baa85-113">Ez a parancs az összes csoportot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="baa85-113">This command gets all groups.</span></span>

### <span data-ttu-id="baa85-114">2. példa: csoport beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="baa85-114">Example 2: Get a group by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -GroupId "0123456789"
```

<span data-ttu-id="baa85-115">Ez a parancs a 0123456789 nevű csoport AZONOSÍTÓját kapja.</span><span class="sxs-lookup"><span data-stu-id="baa85-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="baa85-116">3. példa: csoport beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="baa85-116">Example 3: Get a group by name</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -Name "Group0002"
```

<span data-ttu-id="baa85-117">Ez a parancs a Group0002 nevű csoportot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="baa85-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="baa85-118">4. példa: az összes felhasználó csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="baa85-118">Example 4: Get all user groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -UserId "0123456789"
```

<span data-ttu-id="baa85-119">Ez a parancs a 0123456789 nevű felhasználói AZONOSÍTÓval minden felhasználó csoportba bekerül.</span><span class="sxs-lookup"><span data-stu-id="baa85-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="baa85-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="baa85-120">PARAMETERS</span></span>

### <span data-ttu-id="baa85-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="baa85-121">-Context</span></span>
<span data-ttu-id="baa85-122">A PsApiManagementContext példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="baa85-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="baa85-123">-GroupId</span><span class="sxs-lookup"><span data-stu-id="baa85-123">-GroupId</span></span>
<span data-ttu-id="baa85-124">A csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="baa85-124">Specifies the group ID.</span></span>
<span data-ttu-id="baa85-125">Ha meg van adva, a parancsmag megpróbálja megtalálni a csoportot az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="baa85-125">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by group ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baa85-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="baa85-126">-Name</span></span>
<span data-ttu-id="baa85-127">A felügyeleti csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="baa85-127">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="baa85-128">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="baa85-128">-ProductId</span></span>
<span data-ttu-id="baa85-129">A meglévő szorzat azonosítója</span><span class="sxs-lookup"><span data-stu-id="baa85-129">Identifier of existing product.</span></span>
<span data-ttu-id="baa85-130">Ha meg van adva, akkor a rendszer minden olyan csoportot ad vissza, amelyre a terméket hozzárendeli.</span><span class="sxs-lookup"><span data-stu-id="baa85-130">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="baa85-131">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="baa85-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by product
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baa85-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="baa85-132">-UserId</span></span>
<span data-ttu-id="baa85-133">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="baa85-133">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="baa85-134">Ha meg van adva, a parancsmag minden olyan csoportot ad vissza, amelyre a terméket hozzárendeli.</span><span class="sxs-lookup"><span data-stu-id="baa85-134">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by user
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baa85-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa85-135">-DefaultProfile</span></span>
<span data-ttu-id="baa85-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="baa85-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baa85-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa85-137">CommonParameters</span></span>
<span data-ttu-id="baa85-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="baa85-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa85-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baa85-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa85-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="baa85-140">INPUTS</span></span>

## <span data-ttu-id="baa85-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="baa85-141">OUTPUTS</span></span>

### <span data-ttu-id="baa85-142">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGroup></span><span class="sxs-lookup"><span data-stu-id="baa85-142">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>

## <span data-ttu-id="baa85-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="baa85-143">NOTES</span></span>

## <span data-ttu-id="baa85-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="baa85-144">RELATED LINKS</span></span>

[<span data-ttu-id="baa85-145">Új – AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="baa85-145">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="baa85-146">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="baa85-146">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="baa85-147">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="baa85-147">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


