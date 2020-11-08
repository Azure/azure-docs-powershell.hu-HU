---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: fcedf52f75b73cc35b7f0e4fd0856600bca6fc71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182720"
---
# <span data-ttu-id="0fb1d-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0fb1d-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="0fb1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fb1d-102">SYNOPSIS</span></span>

<span data-ttu-id="0fb1d-103">Megnyeri a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="0fb1d-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="0fb1d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fb1d-104">SYNTAX</span></span>

### <span data-ttu-id="0fb1d-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fb1d-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fb1d-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fb1d-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fb1d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fb1d-107">DESCRIPTION</span></span>

<span data-ttu-id="0fb1d-108">A **Get-AzRecoveryServicesVault** parancsmag az aktuális előfizetésben a helyreállítási szolgáltatások boltozatának listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="0fb1d-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="0fb1d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0fb1d-109">EXAMPLES</span></span>

### <span data-ttu-id="0fb1d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0fb1d-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="0fb1d-111">A kijelölt előfizetésben lévő Vault-lista lekérése</span><span class="sxs-lookup"><span data-stu-id="0fb1d-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="0fb1d-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="0fb1d-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="0fb1d-113">A kijelölt előfizetéshez tartozó Vault-lista lekérése az erőforrás csoportban</span><span class="sxs-lookup"><span data-stu-id="0fb1d-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="0fb1d-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="0fb1d-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="0fb1d-115">Adja meg a boltozatot az erőforrás csoportban a megadott névvel.</span><span class="sxs-lookup"><span data-stu-id="0fb1d-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="0fb1d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fb1d-116">PARAMETERS</span></span>

### <span data-ttu-id="0fb1d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fb1d-117">-DefaultProfile</span></span>

<span data-ttu-id="0fb1d-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fb1d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fb1d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0fb1d-119">-Name</span></span>

<span data-ttu-id="0fb1d-120">A lekérdezni kívánt boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0fb1d-120">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="0fb1d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fb1d-121">-ResourceGroupName</span></span>

<span data-ttu-id="0fb1d-122">Annak az Azure erőforrás-csoportnak a neve, amelyből a megadott helyreállítási szolgáltatási objektumot be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="0fb1d-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="0fb1d-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="0fb1d-123">-Tag</span></span>

<span data-ttu-id="0fb1d-124">A lekérdezéshez szükséges címkéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="0fb1d-124">Specifies the Tags to query for</span></span>

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

### <span data-ttu-id="0fb1d-125">-TagName</span><span class="sxs-lookup"><span data-stu-id="0fb1d-125">-TagName</span></span>

<span data-ttu-id="0fb1d-126">A lekérdezni kívánt címke kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0fb1d-126">Specifies the Key of the Tag to query for</span></span>

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

### <span data-ttu-id="0fb1d-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="0fb1d-127">-TagValue</span></span>

<span data-ttu-id="0fb1d-128">A lekérdezni kívánt címke értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0fb1d-128">Specifies the Value of the Tag to query for</span></span>

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

### <span data-ttu-id="0fb1d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb1d-129">CommonParameters</span></span>
<span data-ttu-id="0fb1d-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fb1d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fb1d-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0fb1d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb1d-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fb1d-132">INPUTS</span></span>

### <span data-ttu-id="0fb1d-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="0fb1d-133">None</span></span>

## <span data-ttu-id="0fb1d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fb1d-134">OUTPUTS</span></span>

### <span data-ttu-id="0fb1d-135">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="0fb1d-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="0fb1d-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fb1d-136">NOTES</span></span>
<span data-ttu-id="0fb1d-137">Az. RecoveryServices (<= 2.10.0) régi verziójában az Get-AzRecoveryServicesVault nem dolgozhat az az. accounts (>= 1.8.1) funkcióval, mert helytelen a kódösszeállítás-hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="0fb1d-137">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="0fb1d-138">Az. RecoveryServices modult frissíteni kell a 2.11.0-ra vagy újabb verzióra, ha a legújabb az vagy az a. fiókot használja.</span><span class="sxs-lookup"><span data-stu-id="0fb1d-138">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="0fb1d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fb1d-139">RELATED LINKS</span></span>

[<span data-ttu-id="0fb1d-140">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0fb1d-140">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="0fb1d-141">Új – AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0fb1d-141">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="0fb1d-142">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0fb1d-142">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
