---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: bdcbac04d621319ac3837f1efaef52018e0f4eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505848"
---
# <span data-ttu-id="09fc1-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="09fc1-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="09fc1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="09fc1-103">Felhasználó eltávolítása egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="09fc1-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09fc1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09fc1-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09fc1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="09fc1-105">DESCRIPTION</span></span>
<span data-ttu-id="09fc1-106">A **Remove-AzureRmApiManagementUserFromGroup** parancsmag eltávolítja a felhasználót egy meglévő csoportból.</span><span class="sxs-lookup"><span data-stu-id="09fc1-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="09fc1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="09fc1-107">EXAMPLES</span></span>

### <span data-ttu-id="09fc1-108">1. példa: felhasználó eltávolítása egy csoportból</span><span class="sxs-lookup"><span data-stu-id="09fc1-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="09fc1-109">Ez a parancs eltávolítja a felhasználót egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="09fc1-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="09fc1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09fc1-110">PARAMETERS</span></span>

### <span data-ttu-id="09fc1-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="09fc1-111">-Context</span></span>
<span data-ttu-id="09fc1-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="09fc1-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="09fc1-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="09fc1-113">This parameter is required.</span></span>

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

### <span data-ttu-id="09fc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fc1-114">-DefaultProfile</span></span>
<span data-ttu-id="09fc1-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09fc1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="09fc1-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="09fc1-116">-GroupId</span></span>
<span data-ttu-id="09fc1-117">Annak a csoportnak az AZONOSÍTÓját adja meg, amelyből a felhasználót el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="09fc1-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="09fc1-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09fc1-118">-PassThru</span></span>
<span data-ttu-id="09fc1-119">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha az $False értéke más.</span><span class="sxs-lookup"><span data-stu-id="09fc1-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="09fc1-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="09fc1-120">-UserId</span></span>
<span data-ttu-id="09fc1-121">Annak a felhasználónak az AZONOSÍTÓját adja meg, akit el szeretne távolítani a csoportból.</span><span class="sxs-lookup"><span data-stu-id="09fc1-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="09fc1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fc1-122">CommonParameters</span></span>
<span data-ttu-id="09fc1-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09fc1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fc1-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09fc1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fc1-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09fc1-125">INPUTS</span></span>

### <span data-ttu-id="09fc1-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="09fc1-126">None</span></span>
<span data-ttu-id="09fc1-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="09fc1-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09fc1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09fc1-128">OUTPUTS</span></span>

### <span data-ttu-id="09fc1-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="09fc1-129">System.Boolean</span></span>

## <span data-ttu-id="09fc1-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09fc1-130">NOTES</span></span>

## <span data-ttu-id="09fc1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09fc1-131">RELATED LINKS</span></span>

[<span data-ttu-id="09fc1-132">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="09fc1-132">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="09fc1-133">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="09fc1-133">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


