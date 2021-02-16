---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f84d233280bc771b90f47c5769fdb6d3f35c2e0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161546"
---
# <span data-ttu-id="e3a99-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="e3a99-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="e3a99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3a99-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a99-103">Az IotHub kapcsolatok kapcsolati kapcsolatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e3a99-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="e3a99-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e3a99-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3a99-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e3a99-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a99-106">Az IotHub kapcsolatok kapcsolati kapcsolatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e3a99-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="e3a99-107">Be is kapcsolhatja az összes kulcs kapcsolatát, vagy adott kulcsnév szerint szűrheti őket.</span><span class="sxs-lookup"><span data-stu-id="e3a99-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="e3a99-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e3a99-108">EXAMPLES</span></span>

### <span data-ttu-id="e3a99-109">1. példa az Összes IotHub-kapcsolati kapcsolat be szereznie</span><span class="sxs-lookup"><span data-stu-id="e3a99-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e3a99-110">A myiothub nevű iothub összes kulcsának kapcsolati kapcsolatát beveszi.</span><span class="sxs-lookup"><span data-stu-id="e3a99-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="e3a99-111">2. példa: Az IotHub kapcsolatokringek lekérte egy adott kulcshoz</span><span class="sxs-lookup"><span data-stu-id="e3a99-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="e3a99-112">A mykey nevű kulcs kapcsolati kapcsolatait kapja a "myiothub" nevű iothubhoz.</span><span class="sxs-lookup"><span data-stu-id="e3a99-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="e3a99-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3a99-113">PARAMETERS</span></span>

### <span data-ttu-id="e3a99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a99-114">-DefaultProfile</span></span>
<span data-ttu-id="e3a99-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e3a99-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3a99-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e3a99-116">-KeyName</span></span>
<span data-ttu-id="e3a99-117">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="e3a99-117">Name of the Key</span></span>

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

### <span data-ttu-id="e3a99-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e3a99-118">-Name</span></span>
<span data-ttu-id="e3a99-119">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="e3a99-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="e3a99-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a99-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3a99-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e3a99-121">Resource Group Name</span></span>

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

### <span data-ttu-id="e3a99-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a99-122">CommonParameters</span></span>
<span data-ttu-id="e3a99-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a99-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a99-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a99-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a99-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3a99-125">INPUTS</span></span>

### <span data-ttu-id="e3a99-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e3a99-126">System.String</span></span>

## <span data-ttu-id="e3a99-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3a99-127">OUTPUTS</span></span>

### <span data-ttu-id="e3a99-128">Microsoft.Azure.Commands.Management.iotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e3a99-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="e3a99-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e3a99-129">NOTES</span></span>

## <span data-ttu-id="e3a99-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3a99-130">RELATED LINKS</span></span>
