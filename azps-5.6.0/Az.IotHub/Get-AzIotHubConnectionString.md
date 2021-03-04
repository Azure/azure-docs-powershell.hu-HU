---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: ba5ab4214de0272338bac61cdf1bbabc9507a9ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936938"
---
# <span data-ttu-id="2db96-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="2db96-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="2db96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2db96-102">SYNOPSIS</span></span>
<span data-ttu-id="2db96-103">Az IotHub kapcsolatok kapcsolati kapcsolatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2db96-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="2db96-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2db96-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2db96-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2db96-105">DESCRIPTION</span></span>
<span data-ttu-id="2db96-106">Az IotHub kapcsolatok kapcsolati kapcsolatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2db96-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="2db96-107">Be is kapcsolhatja az összes kulcs kapcsolatát, vagy adott kulcsnév szerint szűrheti őket.</span><span class="sxs-lookup"><span data-stu-id="2db96-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="2db96-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2db96-108">EXAMPLES</span></span>

### <span data-ttu-id="2db96-109">1. példa az Összes IotHub-kapcsolati kapcsolat be szereznie</span><span class="sxs-lookup"><span data-stu-id="2db96-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2db96-110">A myiothub nevű iothub összes kulcsának kapcsolati kapcsolatát beveszi.</span><span class="sxs-lookup"><span data-stu-id="2db96-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="2db96-111">2. példa: Az IotHub kapcsolatokringek lekérte egy adott kulcshoz</span><span class="sxs-lookup"><span data-stu-id="2db96-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="2db96-112">A mykey nevű kulcs kapcsolati kapcsolatait kapja a myiothub nevű iothubhoz.</span><span class="sxs-lookup"><span data-stu-id="2db96-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="2db96-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2db96-113">PARAMETERS</span></span>

### <span data-ttu-id="2db96-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db96-114">-DefaultProfile</span></span>
<span data-ttu-id="2db96-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2db96-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2db96-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="2db96-116">-KeyName</span></span>
<span data-ttu-id="2db96-117">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="2db96-117">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2db96-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2db96-118">-Name</span></span>
<span data-ttu-id="2db96-119">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="2db96-119">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db96-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db96-120">-ResourceGroupName</span></span>
<span data-ttu-id="2db96-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2db96-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db96-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db96-122">CommonParameters</span></span>
<span data-ttu-id="2db96-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2db96-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db96-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2db96-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db96-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2db96-125">INPUTS</span></span>

### <span data-ttu-id="2db96-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2db96-126">System.String</span></span>

## <span data-ttu-id="2db96-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2db96-127">OUTPUTS</span></span>

### <span data-ttu-id="2db96-128">Microsoft.Azure.Commands.Management.iotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2db96-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="2db96-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2db96-129">NOTES</span></span>

## <span data-ttu-id="2db96-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2db96-130">RELATED LINKS</span></span>
