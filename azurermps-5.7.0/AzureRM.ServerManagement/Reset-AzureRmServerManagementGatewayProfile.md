---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22B63259-799B-4F25-A06B-7A818D295870
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/reset-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 0833266bcd6e98a1d9744db2bc202bce5a01f3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494351"
---
# <span data-ttu-id="678b1-101">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="678b1-101">Reset-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="678b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="678b1-102">SYNOPSIS</span></span>
<span data-ttu-id="678b1-103">A Kiszolgálókezelő-átjárók profiljának alaphelyzetbe állítása.</span><span class="sxs-lookup"><span data-stu-id="678b1-103">Resets the profile of a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="678b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="678b1-104">SYNTAX</span></span>

### <span data-ttu-id="678b1-105">ByName</span><span class="sxs-lookup"><span data-stu-id="678b1-105">ByName</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="678b1-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="678b1-106">ByObject</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="678b1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="678b1-107">DESCRIPTION</span></span>
<span data-ttu-id="678b1-108">A **reset-AzureRmServerManagementGatewayProfile** parancsmag visszaállítja az Azure Server Management átjáró profilját.</span><span class="sxs-lookup"><span data-stu-id="678b1-108">The **Reset-AzureRmServerManagementGatewayProfile** cmdlet resets the profile for an Azure Server Management Gateway.</span></span>

<span data-ttu-id="678b1-109">Az Save-AzureRmServerManagementGatewayProfile parancsmagot kell használnia a profil letöltéséhez, majd a Install-AzureRmServerManagementGatewayProfile parancsmagot a profil visszaállítása után mentenie.</span><span class="sxs-lookup"><span data-stu-id="678b1-109">You will need to use the Save-AzureRmServerManagementGatewayProfile cmdlet to download the profile and then the Install-AzureRmServerManagementGatewayProfile cmdlet to save it after you reset the profile.</span></span>

## <span data-ttu-id="678b1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="678b1-110">EXAMPLES</span></span>

## <span data-ttu-id="678b1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="678b1-111">PARAMETERS</span></span>

### <span data-ttu-id="678b1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678b1-112">-DefaultProfile</span></span>
<span data-ttu-id="678b1-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="678b1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="678b1-114">-Gateway</span><span class="sxs-lookup"><span data-stu-id="678b1-114">-Gateway</span></span>
<span data-ttu-id="678b1-115">Azt az átjárót adja meg, amelyhez a parancsmag visszaállítja a profilt.</span><span class="sxs-lookup"><span data-stu-id="678b1-115">Specifies the gateway for which the cmdlet resets the profile for.</span></span>

<span data-ttu-id="678b1-116">Lehet megadni a ResourceGoupName és a GatewayName helyett</span><span class="sxs-lookup"><span data-stu-id="678b1-116">May be specified instead of ResourceGoupName and GatewayName</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="678b1-117">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="678b1-117">-GatewayName</span></span>
<span data-ttu-id="678b1-118">Annak az átjárónak a neve, amelyhez a parancsmag visszaállítja a profilt.</span><span class="sxs-lookup"><span data-stu-id="678b1-118">Specifies the name of the gateway for which the cmdlet resets the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678b1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="678b1-119">-ResourceGroupName</span></span>
<span data-ttu-id="678b1-120">Annak az erőforráscsoport-csoportnak a neve, amelyhez az átjáró tartozik.</span><span class="sxs-lookup"><span data-stu-id="678b1-120">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678b1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678b1-121">CommonParameters</span></span>
<span data-ttu-id="678b1-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="678b1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678b1-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="678b1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678b1-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="678b1-124">INPUTS</span></span>

### <span data-ttu-id="678b1-125">Átjáró</span><span class="sxs-lookup"><span data-stu-id="678b1-125">Gateway</span></span>
<span data-ttu-id="678b1-126">Az "átjáró" paraméter elfogadja az "átjáró" típusú értéket a csővezetéken</span><span class="sxs-lookup"><span data-stu-id="678b1-126">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="678b1-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="678b1-127">OUTPUTS</span></span>

## <span data-ttu-id="678b1-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="678b1-128">NOTES</span></span>

## <span data-ttu-id="678b1-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="678b1-129">RELATED LINKS</span></span>

[<span data-ttu-id="678b1-130">Telepítés – AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="678b1-130">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="678b1-131">Mentés-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="678b1-131">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


