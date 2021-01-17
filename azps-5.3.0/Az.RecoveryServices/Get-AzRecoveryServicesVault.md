---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: f667c0b13de510f7cf3e30e3faca9a93395ac221
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467250"
---
# <span data-ttu-id="ee9c9-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ee9c9-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="ee9c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee9c9-102">SYNOPSIS</span></span>

<span data-ttu-id="ee9c9-103">Lekérte a Helyreállítási szolgáltatások tárolóinak listáját.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="ee9c9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ee9c9-104">SYNTAX</span></span>

### <span data-ttu-id="ee9c9-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee9c9-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee9c9-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee9c9-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee9c9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ee9c9-107">DESCRIPTION</span></span>

<span data-ttu-id="ee9c9-108">A **Get-AzRecoveryServicesVault** parancsmag lekérte a helyreállítási szolgáltatások tárolóinak listáját az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="ee9c9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ee9c9-109">EXAMPLES</span></span>

### <span data-ttu-id="ee9c9-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="ee9c9-110">Example 1</span></span>

```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="ee9c9-111">A kijelölt előfizetésben található tárolólista lekérte.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="ee9c9-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="ee9c9-112">Example 2</span></span>

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="ee9c9-113">A kijelölt előfizetés erőforráscsoportban található tároló listájának lekérte.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="ee9c9-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="ee9c9-114">Example 3</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

<span data-ttu-id="ee9c9-115">Az első parancsmag a tárolót az erőforráscsoportban kapja meg a megadott néven.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-115">The first cmdlet gets the vault in resource group with given name.</span></span> <span data-ttu-id="ee9c9-116">Ezután hozzáférhetünk az MSI-adatokhoz a tárolóból.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-116">Then we access the MSI information from the vault.</span></span>

## <span data-ttu-id="ee9c9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee9c9-117">PARAMETERS</span></span>

### <span data-ttu-id="ee9c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee9c9-118">-DefaultProfile</span></span>

<span data-ttu-id="ee9c9-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee9c9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ee9c9-120">-Name</span></span>

<span data-ttu-id="ee9c9-121">Megadja annak a tárolónak a nevét, amelyről le kellkérdezni.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-121">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="ee9c9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee9c9-122">-ResourceGroupName</span></span>

<span data-ttu-id="ee9c9-123">Annak az Azure-erőforráscsoportnak a nevét adja meg, amelyből lekéri a megadott Recovery Services-objektumot.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-123">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9c9-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee9c9-124">-Tag</span></span>

<span data-ttu-id="ee9c9-125">Megadja a lekérdezéshez használható címkéket.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-125">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9c9-126">-TagName</span><span class="sxs-lookup"><span data-stu-id="ee9c9-126">-TagName</span></span>

<span data-ttu-id="ee9c9-127">A lekérdezéshez használható címke kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-127">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9c9-128">-TagValue</span><span class="sxs-lookup"><span data-stu-id="ee9c9-128">-TagValue</span></span>

<span data-ttu-id="ee9c9-129">Annak a címkének az értékét adja meg, amelynél a lekérdezést el kell</span><span class="sxs-lookup"><span data-stu-id="ee9c9-129">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9c9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee9c9-130">CommonParameters</span></span>
<span data-ttu-id="ee9c9-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee9c9-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee9c9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee9c9-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee9c9-133">INPUTS</span></span>

### <span data-ttu-id="ee9c9-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="ee9c9-134">None</span></span>

## <span data-ttu-id="ee9c9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee9c9-135">OUTPUTS</span></span>

### <span data-ttu-id="ee9c9-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="ee9c9-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ee9c9-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ee9c9-137">NOTES</span></span>
<span data-ttu-id="ee9c9-138">Get-AzRecoveryServicesVault.RecoveryServices(<=2.10.0) nem működik az Az.Accounts(>=1.8.1) verzióban helytelen összeállítási hivatkozás miatt.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-138">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="ee9c9-139">Az Az.RecoveryServices modult frissíteni kell 2.11.0-s vagy újabb verzióra, ha a legújabb Az vagy Az.Accounts verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-139">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="ee9c9-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee9c9-140">RELATED LINKS</span></span>

[<span data-ttu-id="ee9c9-141">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ee9c9-141">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="ee9c9-142">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ee9c9-142">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="ee9c9-143">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ee9c9-143">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
