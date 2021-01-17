---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: fcedf52f75b73cc35b7f0e4fd0856600bca6fc71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363942"
---
# <span data-ttu-id="61f8a-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="61f8a-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="61f8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61f8a-102">SYNOPSIS</span></span>

<span data-ttu-id="61f8a-103">Lekérte a Helyreállítási szolgáltatások tárolóinak listáját.</span><span class="sxs-lookup"><span data-stu-id="61f8a-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="61f8a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="61f8a-104">SYNTAX</span></span>

### <span data-ttu-id="61f8a-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="61f8a-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61f8a-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61f8a-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61f8a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="61f8a-107">DESCRIPTION</span></span>

<span data-ttu-id="61f8a-108">A **Get-AzRecoveryServicesVault** parancsmag lekérte a helyreállítási szolgáltatások tárolóinak listáját az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="61f8a-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="61f8a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="61f8a-109">EXAMPLES</span></span>

### <span data-ttu-id="61f8a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="61f8a-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="61f8a-111">A kijelölt előfizetésben található tárolólista lekérte.</span><span class="sxs-lookup"><span data-stu-id="61f8a-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="61f8a-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="61f8a-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="61f8a-113">A kijelölt előfizetés erőforráscsoportban található tároló listájának lekérte.</span><span class="sxs-lookup"><span data-stu-id="61f8a-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="61f8a-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="61f8a-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="61f8a-115">Szerezze be a tárolót a megadott nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="61f8a-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="61f8a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61f8a-116">PARAMETERS</span></span>

### <span data-ttu-id="61f8a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f8a-117">-DefaultProfile</span></span>

<span data-ttu-id="61f8a-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61f8a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61f8a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="61f8a-119">-Name</span></span>

<span data-ttu-id="61f8a-120">Megadja annak a tárolónak a nevét, amelyről le kellkérdezni.</span><span class="sxs-lookup"><span data-stu-id="61f8a-120">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="61f8a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f8a-121">-ResourceGroupName</span></span>

<span data-ttu-id="61f8a-122">Annak az Azure-erőforráscsoportnak a nevét adja meg, amelyből lekéri a megadott Recovery Services-objektumot.</span><span class="sxs-lookup"><span data-stu-id="61f8a-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="61f8a-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="61f8a-123">-Tag</span></span>

<span data-ttu-id="61f8a-124">Megadja a lekérdezéshez használható címkéket.</span><span class="sxs-lookup"><span data-stu-id="61f8a-124">Specifies the Tags to query for</span></span>

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

### <span data-ttu-id="61f8a-125">-TagName</span><span class="sxs-lookup"><span data-stu-id="61f8a-125">-TagName</span></span>

<span data-ttu-id="61f8a-126">A lekérdezéshez használható címke kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="61f8a-126">Specifies the Key of the Tag to query for</span></span>

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

### <span data-ttu-id="61f8a-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="61f8a-127">-TagValue</span></span>

<span data-ttu-id="61f8a-128">Annak a címkének az értékét adja meg, amelynél a lekérdezést el kell</span><span class="sxs-lookup"><span data-stu-id="61f8a-128">Specifies the Value of the Tag to query for</span></span>

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

### <span data-ttu-id="61f8a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f8a-129">CommonParameters</span></span>
<span data-ttu-id="61f8a-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61f8a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f8a-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61f8a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f8a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61f8a-132">INPUTS</span></span>

### <span data-ttu-id="61f8a-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="61f8a-133">None</span></span>

## <span data-ttu-id="61f8a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61f8a-134">OUTPUTS</span></span>

### <span data-ttu-id="61f8a-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="61f8a-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="61f8a-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="61f8a-136">NOTES</span></span>
<span data-ttu-id="61f8a-137">Get-AzRecoveryServicesVault.RecoveryServices(<=2.10.0) nem működik az Az.Accounts(>=1.8.1) verzióban helytelen összeállítási hivatkozás miatt.</span><span class="sxs-lookup"><span data-stu-id="61f8a-137">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="61f8a-138">Az Az.RecoveryServices modult frissíteni kell 2.11.0-s vagy újabb verzióra, ha a legújabb Az vagy Az.Accounts verziót használja.</span><span class="sxs-lookup"><span data-stu-id="61f8a-138">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="61f8a-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61f8a-139">RELATED LINKS</span></span>

[<span data-ttu-id="61f8a-140">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="61f8a-140">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="61f8a-141">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="61f8a-141">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="61f8a-142">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="61f8a-142">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
