---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: 300c99926ae7f58a6bf53ba49f3b5b86f243e150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679304"
---
# <span data-ttu-id="a23b2-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="a23b2-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="a23b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a23b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a23b2-103">Felhasználó felvétele egy csoportba.</span><span class="sxs-lookup"><span data-stu-id="a23b2-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a23b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a23b2-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a23b2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a23b2-105">DESCRIPTION</span></span>
<span data-ttu-id="a23b2-106">Az **Add-AzureRmApiManagementUserToGroup** parancsmag felvesz egy felhasználót egy csoportba.</span><span class="sxs-lookup"><span data-stu-id="a23b2-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="a23b2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a23b2-107">EXAMPLES</span></span>

### <span data-ttu-id="a23b2-108">1. példa: felhasználó felvétele egy csoportba</span><span class="sxs-lookup"><span data-stu-id="a23b2-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="a23b2-109">Ez a parancs egy meglévő felhasználót ad hozzá egy meglévő csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="a23b2-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="a23b2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a23b2-110">PARAMETERS</span></span>

### <span data-ttu-id="a23b2-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a23b2-111">-Context</span></span>
<span data-ttu-id="a23b2-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a23b2-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="a23b2-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a23b2-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a23b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a23b2-114">-DefaultProfile</span></span>
<span data-ttu-id="a23b2-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a23b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a23b2-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="a23b2-116">-GroupId</span></span>
<span data-ttu-id="a23b2-117">A csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a23b2-117">Specifies the group ID.</span></span>
<span data-ttu-id="a23b2-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a23b2-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a23b2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a23b2-119">-PassThru</span></span>
<span data-ttu-id="a23b2-120">passthru</span><span class="sxs-lookup"><span data-stu-id="a23b2-120">passthru</span></span>

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

### <span data-ttu-id="a23b2-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="a23b2-121">-UserId</span></span>
<span data-ttu-id="a23b2-122">A felhasználói azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="a23b2-122">Specifies the user ID.</span></span>
<span data-ttu-id="a23b2-123">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a23b2-123">This parameter is required.</span></span>

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

### <span data-ttu-id="a23b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a23b2-124">CommonParameters</span></span>
<span data-ttu-id="a23b2-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a23b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a23b2-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a23b2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a23b2-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a23b2-127">INPUTS</span></span>

### <span data-ttu-id="a23b2-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="a23b2-128">None</span></span>
<span data-ttu-id="a23b2-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a23b2-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a23b2-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a23b2-130">OUTPUTS</span></span>

### <span data-ttu-id="a23b2-131">Logikai</span><span class="sxs-lookup"><span data-stu-id="a23b2-131">Boolean</span></span>

## <span data-ttu-id="a23b2-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a23b2-132">NOTES</span></span>

## <span data-ttu-id="a23b2-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a23b2-133">RELATED LINKS</span></span>

[<span data-ttu-id="a23b2-134">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a23b2-134">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="a23b2-135">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="a23b2-135">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


