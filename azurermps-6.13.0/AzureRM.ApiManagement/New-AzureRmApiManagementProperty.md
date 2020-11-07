---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: bb0fb41409407d6e522c8371042e94501b0e1f54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673188"
---
# <span data-ttu-id="658aa-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="658aa-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="658aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="658aa-102">SYNOPSIS</span></span>
<span data-ttu-id="658aa-103">Új tulajdonság létrehozása</span><span class="sxs-lookup"><span data-stu-id="658aa-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="658aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="658aa-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="658aa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="658aa-105">DESCRIPTION</span></span>
<span data-ttu-id="658aa-106">A **New-AzureRmApiManagementProperty** parancsmag egy Azure API-kezelési **tulajdonságot** hoz létre.</span><span class="sxs-lookup"><span data-stu-id="658aa-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="658aa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="658aa-107">EXAMPLES</span></span>

### <span data-ttu-id="658aa-108">Példa 1: címkéket tartalmazó tulajdonság létrehozása</span><span class="sxs-lookup"><span data-stu-id="658aa-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="658aa-109">Az első parancs két értéket rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="658aa-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="658aa-110">A második parancs létrehoz egy tulajdonságot, és a karakterláncokat kiosztja a $Tagsban címkékként a tulajdonságban.</span><span class="sxs-lookup"><span data-stu-id="658aa-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="658aa-111">2. példa: titkos értéket tartalmazó tulajdonság létrehozása</span><span class="sxs-lookup"><span data-stu-id="658aa-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="658aa-112">Ez a parancs olyan **tulajdonságot** hoz létre, amelynek értéke titkosítva van.</span><span class="sxs-lookup"><span data-stu-id="658aa-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="658aa-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="658aa-113">PARAMETERS</span></span>

### <span data-ttu-id="658aa-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="658aa-114">-Context</span></span>
<span data-ttu-id="658aa-115">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="658aa-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="658aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="658aa-116">-DefaultProfile</span></span>
<span data-ttu-id="658aa-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="658aa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="658aa-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="658aa-118">-Name</span></span>
<span data-ttu-id="658aa-119">A parancsmag által létrehozott tulajdonság nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="658aa-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="658aa-120">A maximális hossz 100 karakter.</span><span class="sxs-lookup"><span data-stu-id="658aa-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="658aa-121">A nevek csak betűket, számokat, pont-, kötőjel-és aláhúzás karaktereket tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="658aa-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="658aa-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="658aa-122">-PropertyId</span></span>
<span data-ttu-id="658aa-123">A tulajdonság AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="658aa-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="658aa-124">A maximális hossz 256 karakter.</span><span class="sxs-lookup"><span data-stu-id="658aa-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="658aa-125">Ha nem ad meg azonosítót, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="658aa-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="658aa-126">-Secret</span><span class="sxs-lookup"><span data-stu-id="658aa-126">-Secret</span></span>
<span data-ttu-id="658aa-127">Azt jelzi, hogy a tulajdonság értéke titkos, ezért titkosítottnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="658aa-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="658aa-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="658aa-128">-Tag</span></span>
<span data-ttu-id="658aa-129">A tulajdonsághoz társított Címkék</span><span class="sxs-lookup"><span data-stu-id="658aa-129">Tags to be associated with Property.</span></span> <span data-ttu-id="658aa-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="658aa-130">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="658aa-131">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="658aa-131">-Value</span></span>
<span data-ttu-id="658aa-132">A tulajdonság értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="658aa-132">Specifies a value for the property.</span></span>
<span data-ttu-id="658aa-133">Ez az érték tartalmazhat házirend-kifejezéseket.</span><span class="sxs-lookup"><span data-stu-id="658aa-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="658aa-134">A maximális hossz 1000 karakter.</span><span class="sxs-lookup"><span data-stu-id="658aa-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="658aa-135">Lehet, hogy az érték nem üres, vagy csak szóközökből áll.</span><span class="sxs-lookup"><span data-stu-id="658aa-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="658aa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="658aa-136">CommonParameters</span></span>
<span data-ttu-id="658aa-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="658aa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="658aa-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="658aa-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="658aa-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="658aa-139">INPUTS</span></span>

### <span data-ttu-id="658aa-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="658aa-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="658aa-141">System. String</span><span class="sxs-lookup"><span data-stu-id="658aa-141">System.String</span></span>

### <span data-ttu-id="658aa-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="658aa-142">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="658aa-143">System. string []</span><span class="sxs-lookup"><span data-stu-id="658aa-143">System.String[]</span></span>

## <span data-ttu-id="658aa-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="658aa-144">OUTPUTS</span></span>

### <span data-ttu-id="658aa-145">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="658aa-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="658aa-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="658aa-146">NOTES</span></span>

## <span data-ttu-id="658aa-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="658aa-147">RELATED LINKS</span></span>

[<span data-ttu-id="658aa-148">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="658aa-148">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="658aa-149">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="658aa-149">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


