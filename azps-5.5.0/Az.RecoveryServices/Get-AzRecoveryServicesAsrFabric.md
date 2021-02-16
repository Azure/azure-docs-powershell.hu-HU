---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: c3bd5ecf7e3561be5f9e6b8d990c40281135982c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169307"
---
# <span data-ttu-id="709ba-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="709ba-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="709ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="709ba-102">SYNOPSIS</span></span>
<span data-ttu-id="709ba-103">Az Azure-webhely-helyreállítási háló részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="709ba-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="709ba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="709ba-104">SYNTAX</span></span>

### <span data-ttu-id="709ba-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="709ba-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="709ba-106">ByName</span><span class="sxs-lookup"><span data-stu-id="709ba-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="709ba-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="709ba-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="709ba-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="709ba-108">DESCRIPTION</span></span>
<span data-ttu-id="709ba-109">A **Get-AzRecoveryServicesAsrFabric** parancsmag egy megadott Azure-webhely-helyreállítási anyag vagy az összes Azure-webhely-helyreállítási anyag tulajdonságait kapja meg egy helyreállítási szolgáltatás tárolóban.</span><span class="sxs-lookup"><span data-stu-id="709ba-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="709ba-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="709ba-110">EXAMPLES</span></span>

### <span data-ttu-id="709ba-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="709ba-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="709ba-112">Visszaadja a tárolóban található összes Azure Site Recovery-anyagát.</span><span class="sxs-lookup"><span data-stu-id="709ba-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="709ba-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="709ba-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="709ba-114">Az xxxx nevű Azure-webhely helyreállítási anyagát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="709ba-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="709ba-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="709ba-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="709ba-116">Az Azure-webhely helyreállítási anyagát adja vissza a xxxx névvel.</span><span class="sxs-lookup"><span data-stu-id="709ba-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="709ba-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="709ba-117">PARAMETERS</span></span>

### <span data-ttu-id="709ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709ba-118">-DefaultProfile</span></span>
<span data-ttu-id="709ba-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="709ba-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="709ba-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="709ba-120">-FriendlyName</span></span>
<span data-ttu-id="709ba-121">Keresse meg az ASR-szövetet a szövet felhasználóbarát nevével.</span><span class="sxs-lookup"><span data-stu-id="709ba-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709ba-122">-Name</span><span class="sxs-lookup"><span data-stu-id="709ba-122">-Name</span></span>
<span data-ttu-id="709ba-123">Keresse meg az ASR-szövetet a szövet neve alapján.</span><span class="sxs-lookup"><span data-stu-id="709ba-123">Search for the ASR fabric by the name of the fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709ba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709ba-124">CommonParameters</span></span>
<span data-ttu-id="709ba-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="709ba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709ba-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="709ba-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709ba-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="709ba-127">INPUTS</span></span>

### <span data-ttu-id="709ba-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="709ba-128">None</span></span>

## <span data-ttu-id="709ba-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="709ba-129">OUTPUTS</span></span>

### <span data-ttu-id="709ba-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="709ba-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="709ba-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="709ba-131">NOTES</span></span>

## <span data-ttu-id="709ba-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="709ba-132">RELATED LINKS</span></span>

[<span data-ttu-id="709ba-133">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="709ba-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="709ba-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="709ba-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
