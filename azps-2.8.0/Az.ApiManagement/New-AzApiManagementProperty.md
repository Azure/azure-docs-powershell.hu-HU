---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
ms.openlocfilehash: 816e1ee8af966e7c0a3c296d3e971d69134c103e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668031"
---
# <span data-ttu-id="69476-101">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="69476-101">New-AzApiManagementProperty</span></span>

## <span data-ttu-id="69476-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69476-102">SYNOPSIS</span></span>
<span data-ttu-id="69476-103">Új tulajdonság létrehozása</span><span class="sxs-lookup"><span data-stu-id="69476-103">Creates a new Property.</span></span>

## <span data-ttu-id="69476-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69476-104">SYNTAX</span></span>

```
New-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69476-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69476-105">DESCRIPTION</span></span>
<span data-ttu-id="69476-106">A **New-AzApiManagementProperty** parancsmag egy Azure API-kezelési **tulajdonságot** hoz létre.</span><span class="sxs-lookup"><span data-stu-id="69476-106">The **New-AzApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="69476-107">Példák</span><span class="sxs-lookup"><span data-stu-id="69476-107">EXAMPLES</span></span>

### <span data-ttu-id="69476-108">Példa 1: címkéket tartalmazó tulajdonság létrehozása</span><span class="sxs-lookup"><span data-stu-id="69476-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="69476-109">Az első parancs két értéket rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="69476-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="69476-110">A második parancs létrehoz egy tulajdonságot, és a karakterláncokat kiosztja a $Tagsban címkékként a tulajdonságban.</span><span class="sxs-lookup"><span data-stu-id="69476-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="69476-111">2. példa: titkos értéket tartalmazó tulajdonság létrehozása</span><span class="sxs-lookup"><span data-stu-id="69476-111">Example 2: Create a property that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="69476-112">Ez a parancs olyan **tulajdonságot** hoz létre, amelynek értéke titkosítva van.</span><span class="sxs-lookup"><span data-stu-id="69476-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="69476-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69476-113">PARAMETERS</span></span>

### <span data-ttu-id="69476-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="69476-114">-Context</span></span>
<span data-ttu-id="69476-115">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="69476-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="69476-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69476-116">-DefaultProfile</span></span>
<span data-ttu-id="69476-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69476-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69476-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69476-118">-Name</span></span>
<span data-ttu-id="69476-119">A parancsmag által létrehozott tulajdonság nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69476-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="69476-120">A maximális hossz 100 karakter.</span><span class="sxs-lookup"><span data-stu-id="69476-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="69476-121">A nevek csak betűket, számokat, pont-, kötőjel-és aláhúzás karaktereket tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="69476-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="69476-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="69476-122">-PropertyId</span></span>
<span data-ttu-id="69476-123">A tulajdonság AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="69476-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="69476-124">A maximális hossz 256 karakter.</span><span class="sxs-lookup"><span data-stu-id="69476-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="69476-125">Ha nem ad meg azonosítót, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="69476-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="69476-126">-Secret</span><span class="sxs-lookup"><span data-stu-id="69476-126">-Secret</span></span>
<span data-ttu-id="69476-127">Azt jelzi, hogy a tulajdonság értéke titkos, ezért titkosítottnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="69476-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="69476-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="69476-128">-Tag</span></span>
<span data-ttu-id="69476-129">A tulajdonsághoz társított Címkék</span><span class="sxs-lookup"><span data-stu-id="69476-129">Tags to be associated with Property.</span></span> <span data-ttu-id="69476-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="69476-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="69476-131">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="69476-131">-Value</span></span>
<span data-ttu-id="69476-132">A tulajdonság értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69476-132">Specifies a value for the property.</span></span>
<span data-ttu-id="69476-133">Ez az érték tartalmazhat házirend-kifejezéseket.</span><span class="sxs-lookup"><span data-stu-id="69476-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="69476-134">A maximális hossz 1000 karakter.</span><span class="sxs-lookup"><span data-stu-id="69476-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="69476-135">Lehet, hogy az érték nem üres, vagy csak szóközökből áll.</span><span class="sxs-lookup"><span data-stu-id="69476-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="69476-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69476-136">CommonParameters</span></span>
<span data-ttu-id="69476-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69476-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69476-138">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="69476-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69476-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69476-139">INPUTS</span></span>

### <span data-ttu-id="69476-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="69476-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="69476-141">System. String</span><span class="sxs-lookup"><span data-stu-id="69476-141">System.String</span></span>

### <span data-ttu-id="69476-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="69476-142">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="69476-143">System. string []</span><span class="sxs-lookup"><span data-stu-id="69476-143">System.String[]</span></span>

## <span data-ttu-id="69476-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69476-144">OUTPUTS</span></span>

### <span data-ttu-id="69476-145">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="69476-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="69476-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69476-146">NOTES</span></span>

## <span data-ttu-id="69476-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69476-147">RELATED LINKS</span></span>

[<span data-ttu-id="69476-148">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="69476-148">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)

[<span data-ttu-id="69476-149">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="69476-149">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


