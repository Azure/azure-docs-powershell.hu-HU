---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: 55ef0d4ef714c1d434915def403f5560244a3697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680841"
---
# <span data-ttu-id="fcbbe-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="fcbbe-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="fcbbe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fcbbe-102">SYNOPSIS</span></span>
<span data-ttu-id="fcbbe-103">Új tulajdonság létrehozása</span><span class="sxs-lookup"><span data-stu-id="fcbbe-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcbbe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fcbbe-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcbbe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fcbbe-105">DESCRIPTION</span></span>
<span data-ttu-id="fcbbe-106">A **New-AzureRmApiManagementProperty** parancsmag egy Azure API-kezelési **tulajdonságot** hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="fcbbe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fcbbe-107">EXAMPLES</span></span>

### <span data-ttu-id="fcbbe-108">Példa 1: címkéket tartalmazó tulajdonság létrehozása</span><span class="sxs-lookup"><span data-stu-id="fcbbe-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="fcbbe-109">Az első parancs két értéket rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="fcbbe-110">A második parancs létrehoz egy tulajdonságot, és a karakterláncokat kiosztja a $Tagsban címkékként a tulajdonságban.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="fcbbe-111">2. példa: titkos értéket tartalmazó tulajdonság létrehozása</span><span class="sxs-lookup"><span data-stu-id="fcbbe-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="fcbbe-112">Ez a parancs olyan **tulajdonságot** hoz létre, amelynek értéke titkosítva van.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="fcbbe-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fcbbe-113">PARAMETERS</span></span>

### <span data-ttu-id="fcbbe-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fcbbe-114">-Context</span></span>
<span data-ttu-id="fcbbe-115">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fcbbe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcbbe-116">-DefaultProfile</span></span>
<span data-ttu-id="fcbbe-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="fcbbe-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fcbbe-118">-Name</span></span>
<span data-ttu-id="fcbbe-119">A parancsmag által létrehozott tulajdonság nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="fcbbe-120">A maximális hossz 100 karakter.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="fcbbe-121">A nevek csak betűket, számokat, pont-, kötőjel-és aláhúzás karaktereket tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcbbe-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="fcbbe-122">-PropertyId</span></span>
<span data-ttu-id="fcbbe-123">A tulajdonság AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="fcbbe-124">A maximális hossz 256 karakter.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="fcbbe-125">Ha nem ad meg azonosítót, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="fcbbe-126">-Secret</span><span class="sxs-lookup"><span data-stu-id="fcbbe-126">-Secret</span></span>
<span data-ttu-id="fcbbe-127">Azt jelzi, hogy a tulajdonság értéke titkos, ezért titkosítottnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-127">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcbbe-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="fcbbe-128">-Tag</span></span>
<span data-ttu-id="fcbbe-129">A tulajdonsághoz társított Címkék</span><span class="sxs-lookup"><span data-stu-id="fcbbe-129">Tags to be associated with Property.</span></span> <span data-ttu-id="fcbbe-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-130">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcbbe-131">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="fcbbe-131">-Value</span></span>
<span data-ttu-id="fcbbe-132">A tulajdonság értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-132">Specifies a value for the property.</span></span>
<span data-ttu-id="fcbbe-133">Ez az érték tartalmazhat házirend-kifejezéseket.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="fcbbe-134">A maximális hossz 1000 karakter.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="fcbbe-135">Lehet, hogy az érték nem üres, vagy csak szóközökből áll.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-135">The value may not be empty or consist only of whitespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcbbe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcbbe-136">CommonParameters</span></span>
<span data-ttu-id="fcbbe-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fcbbe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcbbe-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcbbe-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcbbe-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcbbe-139">INPUTS</span></span>

### <span data-ttu-id="fcbbe-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="fcbbe-140">None</span></span>
<span data-ttu-id="fcbbe-141">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fcbbe-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcbbe-142">OUTPUTS</span></span>

### <span data-ttu-id="fcbbe-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="fcbbe-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="fcbbe-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fcbbe-144">NOTES</span></span>

## <span data-ttu-id="fcbbe-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcbbe-145">RELATED LINKS</span></span>

[<span data-ttu-id="fcbbe-146">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="fcbbe-146">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="fcbbe-147">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="fcbbe-147">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


