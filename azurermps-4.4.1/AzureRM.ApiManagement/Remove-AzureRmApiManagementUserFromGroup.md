---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: 2867e8eec65de040a0da61a1af960abc9797bb18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679122"
---
# <span data-ttu-id="275ce-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="275ce-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="275ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="275ce-102">SYNOPSIS</span></span>
<span data-ttu-id="275ce-103">Felhasználó eltávolítása egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="275ce-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="275ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="275ce-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="275ce-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="275ce-105">DESCRIPTION</span></span>
<span data-ttu-id="275ce-106">A **Remove-AzureRmApiManagementUserFromGroup** parancsmag eltávolítja a felhasználót egy meglévő csoportból.</span><span class="sxs-lookup"><span data-stu-id="275ce-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="275ce-107">Példák</span><span class="sxs-lookup"><span data-stu-id="275ce-107">EXAMPLES</span></span>

### <span data-ttu-id="275ce-108">1. példa: felhasználó eltávolítása egy csoportból</span><span class="sxs-lookup"><span data-stu-id="275ce-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="275ce-109">Ez a parancs eltávolítja a felhasználót egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="275ce-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="275ce-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="275ce-110">PARAMETERS</span></span>

### <span data-ttu-id="275ce-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="275ce-111">-Context</span></span>
<span data-ttu-id="275ce-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="275ce-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="275ce-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="275ce-113">This parameter is required.</span></span>

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

### <span data-ttu-id="275ce-114">-GroupId</span><span class="sxs-lookup"><span data-stu-id="275ce-114">-GroupId</span></span>
<span data-ttu-id="275ce-115">Annak a csoportnak az AZONOSÍTÓját adja meg, amelyből a felhasználót el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="275ce-115">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="275ce-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="275ce-116">-PassThru</span></span>
<span data-ttu-id="275ce-117">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha az $False értéke más.</span><span class="sxs-lookup"><span data-stu-id="275ce-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="275ce-118">-UserId</span><span class="sxs-lookup"><span data-stu-id="275ce-118">-UserId</span></span>
<span data-ttu-id="275ce-119">Annak a felhasználónak az AZONOSÍTÓját adja meg, akit el szeretne távolítani a csoportból.</span><span class="sxs-lookup"><span data-stu-id="275ce-119">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="275ce-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275ce-120">-DefaultProfile</span></span>
<span data-ttu-id="275ce-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="275ce-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="275ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275ce-122">CommonParameters</span></span>
<span data-ttu-id="275ce-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="275ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275ce-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="275ce-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275ce-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="275ce-125">INPUTS</span></span>

## <span data-ttu-id="275ce-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="275ce-126">OUTPUTS</span></span>

### <span data-ttu-id="275ce-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="275ce-127">System.Boolean</span></span>

## <span data-ttu-id="275ce-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="275ce-128">NOTES</span></span>

## <span data-ttu-id="275ce-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="275ce-129">RELATED LINKS</span></span>

[<span data-ttu-id="275ce-130">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="275ce-130">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="275ce-131">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="275ce-131">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


