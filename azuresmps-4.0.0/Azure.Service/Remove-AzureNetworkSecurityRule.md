---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8CDB4C0A-A050-4F65-8CC0-1822D006D772
online version: ''
schema: 2.0.0
ms.openlocfilehash: eb0fe27a664badd5f32b941e80b2c8e2cba2d2a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015869"
---
# <span data-ttu-id="2b755-101">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="2b755-101">Remove-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="2b755-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b755-102">SYNOPSIS</span></span>
<span data-ttu-id="2b755-103">Hálózati biztonsági szabály eltávolítása hálózati biztonsági csoportból</span><span class="sxs-lookup"><span data-stu-id="2b755-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="2b755-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b755-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityRule -Name <String> [-Force] -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2b755-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b755-105">DESCRIPTION</span></span>
<span data-ttu-id="2b755-106">A **Remove-AzureNetworkSecurityRule** parancsmag az Azure Network biztonsági szabályait egy hálózati biztonsági csoportból távolítja el.</span><span class="sxs-lookup"><span data-stu-id="2b755-106">The **Remove-AzureNetworkSecurityRule** cmdlet removes an Azure network security rule from a network security group.</span></span>

## <span data-ttu-id="2b755-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2b755-107">EXAMPLES</span></span>

## <span data-ttu-id="2b755-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b755-108">PARAMETERS</span></span>

### <span data-ttu-id="2b755-109">-Force</span><span class="sxs-lookup"><span data-stu-id="2b755-109">-Force</span></span>
<span data-ttu-id="2b755-110">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2b755-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b755-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b755-111">-Name</span></span>
<span data-ttu-id="2b755-112">A parancsmag által eltávolított hálózati biztonsági szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b755-112">Specifies the name for the network security rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2b755-113">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b755-113">-NetworkSecurityGroup</span></span>
<span data-ttu-id="2b755-114">Azt a hálózati biztonsági csoportot adja meg, amelyre a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="2b755-114">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="2b755-115">**INetworkSecurityGroup** objektum beolvasásához használja az Get-AzureNetworkSecurityGroup parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2b755-115">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b755-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="2b755-116">-Profile</span></span>
<span data-ttu-id="2b755-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="2b755-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2b755-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="2b755-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b755-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b755-119">CommonParameters</span></span>
<span data-ttu-id="2b755-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b755-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b755-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b755-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b755-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b755-122">INPUTS</span></span>

## <span data-ttu-id="2b755-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b755-123">OUTPUTS</span></span>

## <span data-ttu-id="2b755-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b755-124">NOTES</span></span>

## <span data-ttu-id="2b755-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b755-125">RELATED LINKS</span></span>

[<span data-ttu-id="2b755-126">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="2b755-126">Set-AzureNetworkSecurityRule</span></span>](./Set-AzureNetworkSecurityRule.md)


