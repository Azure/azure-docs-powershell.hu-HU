---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: abf9cab8e7e832a6221a25aff40f4d7b7ae55d58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679215"
---
# <span data-ttu-id="ba424-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="ba424-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="ba424-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba424-102">SYNOPSIS</span></span>
<span data-ttu-id="ba424-103">Felhasználó eltávolítása egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="ba424-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba424-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba424-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba424-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba424-105">DESCRIPTION</span></span>
<span data-ttu-id="ba424-106">A **Remove-AzureRmApiManagementUserFromGroup** parancsmag eltávolítja a felhasználót egy meglévő csoportból.</span><span class="sxs-lookup"><span data-stu-id="ba424-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="ba424-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ba424-107">EXAMPLES</span></span>

### <span data-ttu-id="ba424-108">1. példa: felhasználó eltávolítása egy csoportból</span><span class="sxs-lookup"><span data-stu-id="ba424-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="ba424-109">Ez a parancs eltávolítja a felhasználót egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="ba424-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="ba424-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba424-110">PARAMETERS</span></span>

### <span data-ttu-id="ba424-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ba424-111">-Context</span></span>
<span data-ttu-id="ba424-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ba424-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="ba424-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ba424-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ba424-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba424-114">-DefaultProfile</span></span>
<span data-ttu-id="ba424-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba424-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba424-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="ba424-116">-GroupId</span></span>
<span data-ttu-id="ba424-117">Annak a csoportnak az AZONOSÍTÓját adja meg, amelyből a felhasználót el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="ba424-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="ba424-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba424-118">-PassThru</span></span>
<span data-ttu-id="ba424-119">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha az $False értéke más.</span><span class="sxs-lookup"><span data-stu-id="ba424-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="ba424-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="ba424-120">-UserId</span></span>
<span data-ttu-id="ba424-121">Annak a felhasználónak az AZONOSÍTÓját adja meg, akit el szeretne távolítani a csoportból.</span><span class="sxs-lookup"><span data-stu-id="ba424-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="ba424-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba424-122">CommonParameters</span></span>
<span data-ttu-id="ba424-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba424-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba424-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba424-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba424-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba424-125">INPUTS</span></span>

### <span data-ttu-id="ba424-126">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ba424-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ba424-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ba424-127">System.String</span></span>

### <span data-ttu-id="ba424-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ba424-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ba424-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba424-129">OUTPUTS</span></span>

### <span data-ttu-id="ba424-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba424-130">System.Boolean</span></span>

## <span data-ttu-id="ba424-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba424-131">NOTES</span></span>

## <span data-ttu-id="ba424-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba424-132">RELATED LINKS</span></span>

[<span data-ttu-id="ba424-133">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="ba424-133">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="ba424-134">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ba424-134">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


